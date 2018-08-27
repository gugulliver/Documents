
##	Introduction:
	This document is a short record of what I have learn during my internship. It is destined to my tutors
 ( enterprise and school alike) and to the programmers of Frontend International who would like to retake my work.

###	The problematic of the internship was:

	“	The project is to develop a proof of concept of an application. This app is mean to create virtual legacy -it is not here question of legal issues - but more simply to allowed someone to 		pass data to someone else at a given time.
	This require a Database with a live expectancy far superior to the on of a storage hardware, and even superior to the time of existence of a company. 
	Moreover it also need the data to be accessible only by a few individual and only at specifics conditions, this conditions could be the demise of the creator or/and a specific event or date.

	In an other way, a client can create a ‘will/ bequest’, in this file he (and only him) can create and store files intended for specify peoples at determined events.
	At the trigger event the storage could be visible to whom it May concern if all the requirements are fulfill.
	Example:  mr X create an account and a legacy, on it, he add information about a bank account  his children would only see after there 18th birthday. At an other time he add a specific “happy 	birthday” video to each of his children that should come repetitively every years for 5 years.
	”

	To answer this problematic I was given a time to study the multiples possibilities  and I came to the same conclusion that the one initially presented was proposed, or that DLT (as blockchains) where a relevant option given the needs of development.  Needs that are a long term durable database.
It can be point out that there is almost no project that are even close to that idea quit promising, the closest that can be found is a time capsule app ‘the incubate’ app  with 25 years at most of insurance.


This document is structures around questions from relay generals one down to my personal application.



##	First of all, what are DLT?

	Distribute Ledgers Technologies is the name given to databases (ledgers) made of links blocks. That have three particularities:
-first of all, they are virtually immutable, the presence of hashes linking blocks make any modification highly visible.
-They are distributed, multiples nodes possess the integral of the ledger, if a modification is done by any node the others will reject this modification as it will disturb the hashes.
-They relay on divers consensus algorithms to add new blocks to the ledger and so one can not push alone a byzantine block.

The pillars on which they where conceived are : transparency, reliability and incorruptibility.
(Some will add Decentralization and Trust)

##This being said, to what good are they? 
	This method create ledgers that are not hold by a superior authority but can still represent a third man in a transaction, a third man that will be reliable and incorruptible. The first use of DLT (the most simple as it was engineered for that purpose) it the transaction of assets. Those assets can represent an actual physical object (a fish, a car,..) an abstract one (a contract…) or simply a currency it is then case if called a crypto-currency. 

####It should be point out a few issues inherent to this technology:
	it can not support heavy package of data, indeed as it is own by all it would require large storage for all participant. 
An other point is that as they are possess by every one who take part in the network if a non negligible part of this network decided to go against it it is possible to break the whole thing ( however most consensus would require between 33% up to 51% of the network to be malicious)

An other thing that is interesting to know is that the main point of this technologies is to be distributed, but at this point the two greatest blockchain (ie Bitcoin and Etherieum) have not much more than 5000 nodes, and this are the greatest. This technology may have a bright future but nowadays it is still quite small on this scale. 


##	What are the different propositions at this day?

	There is a lot of crypto-currencies, some with no other reasons than to represent a currency other with many different ideas and purposes. The major ones are Bitcoin, Ethereum R3 corda, and some project of Hyperledger. The distinction between this tools and others can be found in the document “ComparaisonOfBlockchains” attached.


There is different type of blockchains, bases on multiples criteria. 
They can be either a “permissioned blockchain network” which  require all user (mostly the  nodes) to be clearly identify and allowed to interact, or Permissionless where anyone can create a new node.

They have different type of consensus that have distinct resistances to errors,
Error tolerant or
BFT (Byzantine Fault Tolerance) ( is said of a consensus that can solved this ‘Byzantines generals problem’)


PoS (proof of stack)
-PoW (proof of work) used by Bitcoin, require time and calculation from the validator
-PoEL (proof of elapse time) is used by sawtooth, some sort of random election
-PBFT (Practical Byzantine Fault Tolerance) , SBFT (Simplified Byzantine Fault Tolerance)
algorithms that can solve at least partially the ‘Byzantines generals problem’
...



##	Deepening on Hyperledger

As I decided to work with an Hyperledger project a quick overview could be appreciate:
The Hyperledger Project made by the Linux foundation host five different projects,Fabric, Sawtooth, Burrow, Indy and Iroha.
-Fabric is the oldest and mean to create a really large and modular distribute ledger use kafka as consensus provider
-Sawtooth, seem close to fabric but less flexible, it has a stricter privacy policy.( use PoET (Proof of Elapse Time) as consensus) 
-Indy is meant to provide identity without storing too much personal data.
-Hyperledger Burrow is a permissioned blockchain node that executes smart contract code following the Ethereum specification.
-Iroha, a "normal" blockchain implement in C++, can run on mobile, have a new BFT algorithm.(is composed of clients an peers)


####note:
-Kafka is a: "Kafka is primarily a distributed, horizontally-scalable, fault-tolerant, commit log."
or a system that recive and distribute messages, it run basic verification and is only fault tolerant.

The two most mature project under the Hyperledger umbrella are Sawtooth and Fabric, the key difference between the two is that Sawtooth supports permissioned and permissionless networks whereas Hyperledger Fabric support only permissioned networks.


This difference leads to a number of other points:
    choice of consensus algorithm (PoET vs Kafka)
    size of the network (Sawtooth can support very large networks)
    type of network (star vs hub and spoke)
    security (Fabric has a prescriptive/well-defined approach through MSPs while Sawtooth has a flexible approach using roles and permissions)
    privacy (Fabric has a unique concept of channels that supports transaction privacy)
    governance (Fabric has a better/tighter governance framework)

[https://www.sdxcentral.com/articles/news/whats-the-difference-between-the-5-hyperledger-blockchain-projects/2017/09/]


##	Basic explanation of Sawtooth :

“Hyperledger Sawtooth, focuses on creating very secure way to handle your smart contracts, with strict rules and consensus.”
Sawtooth have a few particularities like:
Sawtooth transactions family :
	The actions allowed within the blockchain of Sawtooth have to be described in a transaction family, this allowed the creator of the network to limit the possibilities (by example it can make a non Turing-complete language to be sure that no one will ever attack his code this way)
It also give a large flexibility to create and limit what can be done, indeed a function in a transaction family can have more possibilities than a database like that allowed only create query and modify.

Proof of Elapsed Time:
	The consensus of Sawtooth is the “Proof of Elapse Time” it was at first based on a physical specificity of Intel processors but is now allowed for any devise. The idea is that all the computer enrolled in the consensus received a different waiting time, and the first to prove that he wait the time he was given is elected leader.

Many supported languages (and can cohabit ) :
A large panel of language can be used to write transactions families from python, nodeJS, Golang, 

	What was my development about?

The issues: 
		-the DB
	It it inerrant to all distributed ledgers that they can not withstand large amount of data. And on of the objective is to provide any type of data, so we had to find a way to store the files of the clients while keeping the hash inside the Chain. This particular mater is discussed in an other document attached, ‘AboutTheStorageOfData’.

		-the time triggered
	This one have stopped me, indeed as all data on a blockchain are accessible through the installation of a node, they are then to be encrypted, but to be read by someone at some time mean two time encrypted. An as to allowed the access to data to peoples that does not yet have the app or a mean to be contacted, the first code must be given an other way (i.e. physically).  The other key can not be on the blockchain (where it could be read by anyone).


##What have I reach ?

I came to the conclusion that this technologies had a conception flaw for our use, indeed the security on a blockchain is only maintained by cryptography and we needed for the app to work two layer of encryption, on for the identity fully untruest to the Clients (receivers and creator) and one for the events entrusted to us. But this mean that we must keep our keys outsides of the blockchain, else the receiver could forced his access through the database with only his identification key. This obligation for us to keep a server in order to maintain the app go against the concept of blockchains.
(it could also be point out tat a few nodes could have been isolated and lured into giving there data through malicious messages).


