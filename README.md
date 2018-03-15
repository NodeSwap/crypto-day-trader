# Crypto Day-Trader
[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/jcvilap/artificial-trader)

## Milestones
#### Setup
- [x] Set up a Node server and deploy it to Heroku
- [x] Setup a Mongo instance in mLab and connect to it from Node
- [ ] Deploy Client app to Surge.sh and point server calls to server's APIs

#### Server
- [x] Connect to GDAX sandboxes for development and production environment 
- [x] Handle security based on GDAX/Coinbase account
- [x] Listen to changes on crypto-currencies
- [x] Hold feeds in a local data structure
- [x] Fetch user account info from GDAX
- [x] Define `Rule` class
- [x] Fetch user `rules` from database
- [x] Enable Buy/Sell, Taker/Maker actions based
- [x] Perform transactions based on `rules`
- [ ] Expose a REST API to fetch user information, performance and any stored transaction(mode to come here...)
- [ ] Expose a WebSocket API to fetch feeds on both user performance and GDAX feeds
- [ ] Alert via email/SMS/native notifications when a transaction happened

### Client
- [ ] Enable new users to enter their Coinbase credentials
- [ ] Enable user to create or reuse rules. Which will affect the percentage-risk for automated trading
- [ ] Enable user to start/stop their artificial traders
- [ ] Connect via Websockets to show transactions realtime
- [ ] Show history and performance 

## Docs
### 3rd Party APIs
- Crypto-currencies exchange feeds and order management: [GDAX Websocket Client](https://github.com/coinbase/gdax-node#websocket-client)

### Rules
I define a `Rule` as a single instance of multiple trading strategies to be used by the `Engine`. Rules can be defined by the user and will be stored in the Mongo instance

### Additional thoughts:
- Create both Desktop and Web versions and share the code as much as possible
- Enable the user to select what currency to watch
- Enable user settings in general including the above mentioned and also rules created and current rules used
- Enable notifications by email or text messages. Also use the native notifications API in the browser

### License

Copyright (c) 2018 Mauer Principles Inc

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

