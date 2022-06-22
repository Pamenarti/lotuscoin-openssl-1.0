# Lotuscoin

NOTE:  This version is for systems running OpenSSL 1.0
For up-to-date OpenSSL compatibility use:
https://github.com/Pamenarti/lotuscoin

--------------------------------------------

The Lotuscoin chain is a log structured database.

The money supply is logarithmic.

The unit is log.
 
--------------------------------------------

Technical Details:
```
* RPC Port = 9338

* P2P Ports = 8338 (testnet 18338)

* In Wallet woodcutting = Console, "setgenerate true"

* 120 Second Block Target, Diff Retarget every 1 hour

* 30 Confirms for spendable-coins

* Block reward = Harmonic Series

* 1000000/nHeight logs  (after first 100 blocks which form unspendable forest of 5187377 logs) 

* Money Supply = 1000000*(log(nHeight) + gamma)     gamma=Euler-Mascheroni constant 

* New ECDSA curve: X9_62_prime256v1 

* Algo = Pure Skein (double skein) 
```
--------------------------------------------

## Build Instructions

TYou will need these dependencies or equivalent:
```
sudo apt-get install build-essential autoconf libboost-all-dev libcurl4-openssl-dev libdb-dev qt-sdk libminiupnpc-dev  openssl libzmq3-dev libevent-dev libssl-dev libminiupnpc-dev libtool libdb++-dev libqrencode-dev 
```
Get the source with this command:

git clone https://github.com/Pamenarti/lotuscoin.git

To build lotuscoin-qt issue “qmake” and then “make“.  qt4 is required, on some systems you may need to issue “export QT_SELECT=qt4” to ensure the proper version is used.

To build lotuscoind by itself navigate to /src/ and issue make -f makefile.unix.

--------------------------------------------
## Mining (Lotuscutting)

To start lotuscutting with lotuscoind, simply launch it like this: 

```./lotuscoind setgenerate true```

For the graphical client, simply go into the debug window (under Help) and type:

```setgenerate true```

--------------------------------------------


### Visit Lotuscoin.xyz for more information. 
