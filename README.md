bitcoin-exchange
================
The purpose of this project is to build a decentralized p2p exchange where client orders 
are matched in one decentralized exchange to enable both local and global trading of digital and physical assets. 
This exchange will consist of many virtual exchanges created by broker alliances.

Any asset can be traded can be traded against any other asset in this exchange and fees are paid in bitcoin.
This exchange-broker model is a simplified model of the CME Globex exchange handling futures contracts.

Inspiration: github.com/bitcoin, #Bitcoin-OTC, github.com/bitcoinx, github.com/macourtney/Dark-Exchange, github.com/FellowTraveler/Open-Transactions, github/?/p2pool, 
retroshare.sourceforge.net, Ripple.com, CME Group, 


## Exchange:
* The exchange network is built with the bitcoin network as inspiration. 
* The network has a blockchain of orders that gets processed by miners willing to participate and get rewarded 
from the brokers with one bitcoin for each N orders that are forwarded in to the exchange. 
* Order matching is done once every block, and each block should take 10 seconds to complete. 
* The order matching is deliberately slow to prevent High Frequency Trading algorithmis having 
advantage over the rest of the market. The orders are not executed as FIFO but in random order as a second protection 
against HFT. 
* Once the orders are matched it is up to the brokers to settle the traded assets.
* Transaction history of executed orders will be saved in the blockchain as evidence if dispute would occur between brokers and clients
* Brokers need to create unique client ids for each of their clients, but the real identity of the client will only be known by the broker. 

## Assets:
* Assets can be both digital or physical, example: cryptocurrencies, digital fiat currencies, physical fiat currencies, gold and silver coin, barrel of gasoline
* Any asset pair can be traded in the exchange just as in a futures exchange since no real asset 
is handled through the exchange itself, only orders of assets. 
* An asset pair can be: Bitcoin traded in US Dollar, BitCoin in Euro, 1 Oz Gold in BitCoin, 1 Oz Silver in BitCoin, LiteCoin in BitCoin, Euro in Dollar, 1 Barrel of Gasoline in Gold
or whatever asset pair the brokers wishes to enable trading in.


## Clearinghouse:
"A clearing house is a financial institution that provides clearing and settlement services for financial and commodities derivatives and securities transactions. 
Once a trade has been executed by two counterparties either on an exchange, or in the OTC markets, the trade can be handed over to a clearing house which then steps between the two original traders' clearing firms and assumes the legal counterparty risk for the trade. This process of transferring the trade title to the clearing house is called novation. It can take fractions of seconds in highly liquid futures markets; or days, or even weeks in some OTC markets."
http://en.wikipedia.org/wiki/Clearing_house_(finance)
* Trust is used instead of a clearing house - the brokers are responsible for the actual transfer of 
assets between the traders. 
* Voluntary rating of the brokers from the clients could be used to indicate the trustworthiness of each broker.

## Brokers and virtual exchanges
"A broker is an individual or party (brokerage firm) that arranges transactions between a buyer and a seller, 
and gets a commission when the deal is executed." (http://en.wikipedia.org/wiki/Broker)

* Anyone can become a broker in this exchange.
* A broker must either join an existing virtual exchange or create a new virtual exchange where orders will be executed. 
* Each broker wishing to join a virtual exchange must be approved by the founder of the virtual exchange which is done by mutual exchange of certificas.
* All brokers should use .bit domains as a backup domain
* Two classes of brokers: Class A Broker can settle assets with brokers in other jurisdictions, Class B Broker can only settle assets with a Class A Broker in the same jurisdiction.
* Each broker has its own order book, and its own asset pairs.
* The brokers using this exchange can have clients globally or locally.
* Client orders are always forwarded to the exchange by the brokers. Clients dont need internet access 
from the exchanges perspective since the clients will never use the exchange directly. 
* If several brokers trust each other they can form a broker-pool by adding each other as trustworthy. Their order books will merge for each asset pair they have in common and all of their clients orders will get matched together in this pool.
* Independent brokers that are not part of a broker-pool have an isolated order book in the exchange, their clients will not be able to trade with clients of the other brokers.
* Settlement of assets should be made on a regular basis (daily or weekly) between brokers in a broker-pool in order to minimize the possible loss off assets in
the event of fraud or default.
* Each broker must comply by local laws in the jurisdiction where the broker is located. 
* Any legal issue is a matter between brokers in a virtual exchange or between a broker and its clients.
* The exchange itself cannot be held responsible for any complaints.

## Questions:
* If the exchange should work as a stock exchange instead of a futures exchange: How to prevent short selling assets that the client dont own and the broker cannot lend on the market?
* Minimum trading size to prevent order spamming? (0.1 BTC)
* Even trading sizes? (0.1, 0.2, 0.3 ...BTC)
* Clearing houses or two classes of brokers? 
* Market makers?
* Darknet?
* Digital tokens to represent the traded assets and wallets to handle the tokens?
* Allowing creation of alliances between virtual exchanges?

Discussion on: https://bitcointalk.org/index.php?topic=172705.0;topicseen
