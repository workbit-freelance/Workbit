WORKBIT Core integration/staging repository
=================================================

WORKBIT (WORKBIT)

- Fast transactions featuring guaranteed zero confirmation transactions, we call it _SwiftTX_.
- Masternode is collateral of 10,000 WORKBIT.



(Above this line = original README.md from WORKBITProject - sample source)
------------------------------------------------------------------------------


(Below are my basic preparation for the practice)


Genesis Block & Merkle hash Info
================================

* Generated:

algorithm: quark

pzTimestamp: Class by Professor Tfinch 2019

pubkey: 04b6209d7542dd5b6daddb677e0df8020f4e9ab5684c313886127e02cde0ff19f3ea1d4c97af94bbeb15a1436930a884c3bb2cbf6cb69dcf530e8fcc972d24c001

bits: 504365040

time: 1551172275

merkle root hash: b5789963fe108433109c84283c86a7c2b95a55c176762130f967215fbbe1bf2b

Searching for genesis hash...

nonce: 1168826

genesis hash: 00000ef21d678d256b9bc3a3bc0c7c5ec2926a3301408f4d528700e0827082eb


SAMPLE KEY1 (vAlertPUBkey used above)
04b6209d7542dd5b6daddb677e0df8020f4e9ab5684c313886127e02cde0ff19f3ea1d4c97af94bbeb15a1436930a884c3bb2cbf6cb69dcf530e8fcc972d24c001

SAMPLE KEY2 
0423b7af794ec13770d98f5aa1f3956f2df8f6a03867459890f96e4ea77628384f8962bbd7c64286b6794b3341aac7d8d8e9a7df63884e505f8882f69911322264

SAMPLE KEY3
049f58cf48a5e38b2f8af1c29c233a805fe818a3084122bdbc84469405d92b3bdc49b890b3e41bf006fe1d223c5a692557271b161efa4f37643bb5621aa9482cd3


[List of Address Prefixes](https://en.bitcoin.it/wiki/List_of_address_prefixes)


//printf("genesis.nTime = %u \n", genesis.nTime.ToString().c_str());

//printf("genesis.nNonce = %u \n", genesis.nNonce.ToString().c_str());

//printf("genesis.nBits = %u \n", genesis.nBits.ToString().c_str());   //(after debug.txt mentioned wrong nBits)

//printf("genesis.GetHash = %s\n", genesis.GetHash().ToString().c_str());

//printf("genesis.hashMerkleRoot = %s\n", genesis.hashMerkleRoot.ToString().c_str());

----------------------------------------------------------------------------------

k@k-VirtualBox:~/Desktop/PracticeClass101/src$ ./WORKBITd

genesis.GetHash = 76e0e633ae0102cbb6935d7896c204c4bccd66f0b2966d304be1e1cbbd7a85c0

genesis.hashMerkleRoot = ce94b6c141f89fd2515763a81701a984e430bada2b31f071b63f038b62b9de2c

WORKBITd: chainparams.cpp:142: CMainParams::CMainParams(): Assertion `hashGenesisBlock == uint256("0x00000ef21d678d256b9bc3a3bc0c7c5ec2926a3301408f4d528700e0827082eb")' failed.
Aborted (core dumped)

k@k-VirtualBox:~/Desktop/PracticeClass101/src$ 


* True value (after ./WORKBITd) :

- Genesis : "0x76e0e633ae0102cbb6935d7896c204c4bccd66f0b2966d304be1e1cbbd7a85c0"

- Merkle hash : "0xce94b6c141f89fd2515763a81701a984e430bada2b31f071b63f038b62b9de2c"

- correct nBit : 


----------------------------------------------------------------------------------

Name & Port changes
===================

find . -type f -print0 | xargs -0 sed -i 's/WORKBIT/WORKBIT/g'

find . -type f -print0 | xargs -0 sed -i 's/WORKBIT/WORKBIT/g'

find . -type f -print0 | xargs -0 sed -i 's/WORKBIT/WORKBIT/g'

find . -type f -print0 | xargs -0 sed -i 's/WORKBIT/WORKBIT/g'

find . -type f -print0 | xargs -0 sed -i 's/WORKBIT/WORKBIT/g'

find . -type f -print0 | xargs -0 sed -i 's/WRB/WRB/g'

find . -type f -print0 | xargs -0 sed -i 's/8888/8888/g'  //(P2P)

find . -type f -print0 | xargs -0 sed -i 's/8887/8887/g'  //(RPC)

find . -type f -print0 | xargs -0 sed -i 's/18888/18888/g'  //(P2P) -testnet

find . -type f -print0 | xargs -0 sed -i 's/18887/18887/g'  //(RPC) -testnet


Before compile
==============

chmod u+x share/genbuild.sh && chmod u+x src/leveldb/build_detect_platform

chmod u+x ./autogen.sh && ./autogen.sh

./configure --disable-dependency-tracking --enable-tests=no --without-gui --without-miniupnpc

make

make install

