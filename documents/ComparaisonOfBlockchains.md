#	Comparison  of technologies regarding blockchains and distribute Ledgers

	During my firsts weeks at Frontware International I tried to get the maximum of information on the DLT which was a new thing for me to work with. 
It must be noticed in first place that the need for a DLT in itself is not obvious, but in this particular case it allowed (and is the only way presently) to answer to one of the biggest requirement of this project:
	Resilience of data over decades even in the event of the demise of the company or any other 	participant of the project. For this matter the distribute technologies are what is the closer to a 	perfect data-base. However, they do not possess all qualities and lack of two things at this point: 	a large capacity of stock, and a reliable clock. 
Mea-culpa : By construction the data on a blockchain cannot be secured by date and by reader at the same time without a third  party, either you do not know the key to read the data that have been sent to you, either the clock is not on the chain.

##	The major existing Distribute Ledger are:

###BigChainDB,
an open source system that “starts with a big data distributed database and then adds blockchain characteristics — decentralized control, immutability and the transfer of digital assets”.
BigchainDB is not designed to support large binary payloads. For this case it is recommended to hash the content and link to it in another database, such as IPFS or S3. Itis meen for storing, indexing and querying structured data, not files.
If you want decentralized file storage, check out Storj, Sia, Swarm or IPFS/Filecoin.
no examples or tutorial. Hard to create node (for the moment)
the technology is more suitable for private blockchains. Reach 2.0 but cannot find anything working on v1…
Not enough flexible, is not mean to be edited. Is into a new project (IPLD)(quite nice btw) which is a world computer and it is absolutely not what we are looking for.
redemption point: it allowed to put file, to add owners, to transfer them … this assets can be of any type and with tendermint it is (supposedly) BFT 
BigchainDB is easier to start with as it is composed of just a few functions. Hyperledger Fabric involves a lot of more knowledge to master it.

###Corda,
 a distributed ledger platform with pluggable consensus. Is a permissioned network and the consensus is reached through the parties involved in the transaction. Consensus is achieved via Transaction validity (Smart contract run to ensure that the required signatures are obtained) and Transaction Uniqueness (To ensure that the transaction is the unique consumer of all the input).
-Really law oriented, it was mean to create legal contracts, or exchange with banks.
“Diverse industries such as finance, supply chain, trade finance, healthcare and government can use Corda to simplify business transactions” 
allowed to code in Java
[https://www.corda.net/]
“The smart contracts in Corda contains code and additionally contains a legal prose (Ricardian Contract). The smart contracts are written in kotlin or java. Corda has been explicitly designed for the highly regulated environment of the financial services industry.”


###Ethereum,
 a decentralized platform that runs smart contracts on a custom built blockchain. It follows a permissionless network. It is one of the most used DLT, but it needs Ether (its cryptocurency) to run and is mainly editable in Solidity, in addition it is still on a PoW consensus (The consequences are that it impacts the performance of the transaction processing as the number of participants can be high). However, it must be point out that Ethereum help developers to create app and already possess a distributed database (Sia). Ethereum framework pays the nodes in the form of the virtual currency “Ether”, which help in the process of mining blocks to reach consensus. The smart contracts in Ethereum are written in Solidity.

###Hyperledger Fabric,
 which supports the use of one or more networks, each managing different Assets, Agreements and Transactions between different sets of Member nodes. Is a permissioned network (as the BFT is not yet implemented) Thus enhances the privacy and also the performance is improved. Unlike Ethereum, fabric provides different roles to the participants within the network (Ex: Peers, Endorsers and Orderers). The smart contracts in fabric are written in Go or java and they are termed as “Chaincode”. Fabric does not require a crypto currency for mining to reach consensus.
Fabric is a modular blockchain platform and applicable across industries.
-Useful, but not (yet) mean to be deployed for real, lack of real strong consensus.
It is only a permissioned blockchain network, and we need a more permissionless one for people to create nodes without heavy validation process.

###Bitcoin,
 the most old and used one here, it is  possible to create and launch your own private network but , it is not really useful a it follow a PoW consensus. Some application are relaying on the Bitcoin blockchain to run (like some stamps app) but the transactions are small and costly.

###Hyperledger Iroha,
 a “simple and modularized” distributed ledger system with emphasis on mobile application development.
-can have higher performance for small data...

###Hyperledger Sawtooth,
 a modular blockchain suite in which transaction business logic is decoupled from the consensus layer.
Mean to be largely scalable and have a few working examples

###Multichain,
 an open-source blockchain platform, based on bitcoin’s blockchain, for multi-asset financial transactions.
[https://www.multichain.com/]

###Openchain,
 an open source distributed ledger system for issuing and managing digital assets.
(astonishing…) is mean to create private network with a manager.
Still in version 0.7
[https://www.openchain.org/]


Note: they are all open sources
