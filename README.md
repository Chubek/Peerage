# Peerage

Peerage (pronounced peer-aazh not peer-age!) is a P2P communication and file sharing tool  with monetization abilities. The app is made of "rooms" and these rooms are customizable through HTML, CSS and JavaScript. But the room resides on your PC, not a server, and anyone who connect to your room accepts some of the load. Peers discover each othr through a ledger and muliicast DNS.  Speakinh of ledgers you can make your room VIP and have people who pay the token registered in the ledger to acces it. The token is not a cryptocurrency, it's not mined or anything, it's just, like, a representation for the other cryptocurrencies. You basically pay in crypto to buy this token and the token is in the ledger... you know, like NeoPets currency but P2P! I had originally written 'our token' but that's wrong, the token does not belong to anyone but the holder. This is entirely decentralized. You can do "other" things with this token too. The ledger is shared by all members, only one aspect of ledger is active (aka uncompressed) active at time. The other aspects are compressed.

As far as the network is concerned, I, being a hip young go-getter (I'm 29 but I have to get dentures :( take care of your teeth kids!) will use QUIC as the main transport. I will use come up with common discovery and multicast methods too. All these will be of my own implementation, although I might copy off libp2p like the loser that I am. But I won't use libp2p. I still have to plan the network side of thing, but it will siurely be planned by late this month.

So, every room has a ledger head, an storage middle, and a cryptographic end. Each of these sections are what make of a 'Rapid Tree' which I have explained below.

![](levels.png)

That is because we will have rooms that are just ledgers, but we will have rooms with storage, say an HTML page or something like that, or a music file, that that the ledger controls. For example, the ledger can control who has bought an item. 


Cryptographic data are for data that need to be hidden. This includes secret financial data or similar things. 

One thing ledger could control is the financial data, as in, if the rom is VIP, who hs paid for it with what crpto, etc.

The development on RapdiTree is onoing.

It's highly WIP. Any financial support during the development of this application is appreciated. Also you can do pull requests. 


## What I have made so for

### Peerage-Utils

This project contains all the utilities. Right now it hosts traits and this MASSIVE binary tool I have written. 


### Peerage-Hash

The custom hash that I am going to use all across the software. It's kinda slow curently but I will work on it to make it faster.

### Peerage-Coll

I need my RapidTree data to live on the stack(it allows me so much suff especially use of Copy). So I made peerage-coll.

A dynamic list, like any dynamic list, I am using Rust arrays to hold the dat and it can be turned into an iterator as well (nothing spectial, I just created an iterator wrapper and implemented IntoIter. I will implement from iter too but there's already a function for that). The dynamic list (which I call "collection") has a macro (`coll!`) too, just like vec.

The maximum length it can hold is `1024 * 16` but I don't need more than that, I doubt it will have more than 100 items.

### Peerage-RTree

I have created this datatype for holding the room data and the Merkle DAG required called 'Rapid Tree'. Keep in mind that I am currenctly working  on it so it's not completed yet.

Basically, it's B-Tree mixed wih some B+Tree mixed with some BTreeMap.

### Peerage-Macros

The necessary proc macros.

### Peerage-Holder

This is a holder enum, a bit like Option, a bit like Box. I need to rework it a bit. It can be used to hold several types into one type.



The rest of the projects are empty, don't bother. But slowly, they will be filled.


### I wanna help! What should I do?

Since all I've been doing instead of my job is this, my boss must be rather cross with me --- insomuch that he has not paid me for a while. So any amount is appreciated.

You can help me by "buying me a coffee" (but I'm not going to buy coffee with it lol gonna buy tea).

![](coffee.png)

Send me any amount you can to this ERC20 Ether address. 


`0x503A3B99c0c086fD81186a0d5ac815eBd15e5983`

It's protected by Nano S Ledger hardware wallet, I bought it the moment I started working in crypto. PLEASE buy a hardware wallet! You can use them through MetaMask!

Note: After you donate to me tell me in Discord (if you want) sO I can add you to patron lis. 

## Final Words

This is a dream I have and as you can see I am going forward, changing things, finalizing things, it would be great if my needs are taken care of, I don't need much money --- I can live off with 300 USD a month. Yes I am e-begging but I don't care. I know Peerage is going ot be revolutionary, something great, something I can be proud of.


## I hate/love/admire this project, where can I find you?

Find me on Discord where you can give me criticism, insult me, or send me a heart emoji (a RED one!).

My Discord: Chubak#7400