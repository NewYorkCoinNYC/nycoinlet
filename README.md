nycoinlet
=======

Dead simple newyorkcoin wallet app in Node.JS with coffeescript. It was built as a test of the module [node-newyorkcoin](https://github.com/NewYorkCoinNYC/Node-NewYorkCoin) , which it uses to connect to newyorkcoind via json-rpc.

You'll have to install [newyorkcoind](https://github.com/NewYorkCoinNYC/nycoin) first.

Then clone this wallet and install deps with npm.

```

git clone https://github.com/NewYorkCoinNYC/nycoinlet.git
cd nycoinlet
npm install .

```

Then create a local config file. It is in the .gitignore if you do this, so your sensitive info isn't shared:

```

cp config.coffee.template config.coffee

```

Then fill out all the values in config.coffee for your system. Remember to compile any coffee file after changing it.

```

coffee -c config.coffee

```

Then run the web app.

```

node app.js

```

And, you should be able to browse to the wallet on localhost:3000

This wallet currently uses sendgrid for email, and redis for storing sessions, but it's easy to change this.

