
#	The different distributed data-bases

	For the database, it can be either centralize or distributed. If centralize it means to use Amazon,
 Google, any other company or our own servers (the point of using our own servers is rejected by principle).
 We could use a DBaaS company but in this case it would mean to forfeit our insurance to their. 

The use of cooperative storage cloud seems quite logic related to the main goal(ie: store data in a way it 
could never be lost) and technology use (there is a close relation between distributed databases and ledgers).
 However this represent a greatest challenge as the few that exists are not fully ready and for some not even 
close from being used in this way.
The presently project that are large squall, wildly distributed, fully decentralized are:

###	-StorJ,
 is the biggest one and most well developed, but it is unavailable for the moment as in
 	great changes. It has a great support and is quite user-friendly. The network is more
 	decentralized and secure than centralized alternatives, though you do have to trust the Storj
 	portal to use the network.
	[https://storj.io/]
 	Moreover it is passing (if not already) on the Ethereum blockchain.

###	-Sia,
 Sia has its own blockchain, but is still on heavy development and is not yet very usable.
 	And it still needs you to download the full chain if you want to interact. (it is a small team 2~5
 	that do what they can, but are maybe not as effective as a full-size development team)
	[https://sia.tech/]
	note: it is quite close to R3 and also mean to work mainly with banks, states and other great 	institutions.

###	-Filecoin (IPFS),
 hasn't launch yet, its objectives are high, one of the biggest cons that can be
 	found is that it is quite greedy for the moment. It can be observe that it will be quite effective.
	[https://filecoin.io/]

This are the first three and largest ones (note: they are all open source, and all uses cryptocurrency).
This type of highly distributed database are not the only thing that exist, other categories as distribute database or files system.
This document present a large range of software that exist and provides divers support for the management of data.
Below are presented some solution on different point of development and use.


Close from fully distributes database as the first three but more complicated or less mature.

###	-IPFS,
	in v 0.30.0 : IPFS is a new peer-to-peer hypermedia protocol that aims to supplement, or
 	possibly even replace, the Hypertext Transfer Protocol 
	[https://ipfs.io/]

###	-Peergos,
	 distribute database base on P2P
	alpha release coming soon … (the same that the first three but more axes on security and less 	advance)
	[https://peergos.org/]

###	-Tahoe-LAFS,
	working, in 1.12 and seam usable
	this is a “Free and Open decentralized cloud storage system. It distributes your data across
 	multiple servers. Even if some of the servers fail or are taken over by an attacker, the entire file
 	store continues to function correctly, preserving your privacy and security.”
	sing a Tahoe-LAFS client, you turn a large file into a redundant collection of shares referenced
 	via a filecap. Shares are encrypted chunks of data distributed across many storage servers.
	[https://www.tahoe-lafs.org/]


Tahoe LAFS seems to be the most modular one thanks to its peer-to-peer approach. I looked also at Ceph but it creates an internal topology relaying on a static IP mapping which makes it hard to use in a dynamic and containerized environment.



	-Symform Was among the first distributed database in 2009 (closed in 2016 caused by there
 	non adaptation to the current meta) just  there to
  	show that it existed 

##System file storage

###	-Swarm
	Swarm’s broader objective is to provide infrastructure services for developers of decentralised
 	web applications (dapps), notably: messaging, data streaming, peer to peer accounting, mutable
 	resource updates, storage insurance, proof of custody scan and repair, payment channels and
 	database services.
	[https://swarm-gateways.net/bzz:/theswarm.eth/]
	The Swarm public gateways are temporary and users should not rely on their existence for
 	production services.



###	-Gluster,
	 GlusterFS is a scalable network file system suitable for data-intensive tasks such as 	cloud storage and media streaming
	[https://www.gluster.org/]
	GlusterFS is latency dependent. Since self-heal checks are done when establishing the FD and
 	the client connects to all the servers in the volume simultaneously, high latency (mult-zone)
 	replication is not normally advisable. Each lookup will query both sides of the replica. A simple
 	directory listing of 100 files across a 200ms connection would require 400 round trips totaling
 	80 seconds. A single drupal page could take around 20 minutes.
	Need a Fedora 26 (or later) virtual machine …

###	-Ceph,
	Ceph s a free-software storage platform, implements object storage on a single distributed
 	computer cluster, and provides interfaces for object-, block- and file-level storage. 
	[https://ceph.com/]
	It is quite complicate do deploy, big company oriented.

###	-Dat project,
	 Dat is a new p2p hypermedia protocol. It provides public-key-addressed file
 	archives which can be synced securely and browsed on-demand.
	[https://datproject.org/]
	Dat is a nonprofit-backed data sharing protocol for applications of the future.
	Made for file transfer not file storage? (assure that it is mean to build app, cant find any)

###	-Minio,
	 easy to use and well developed
	“we have decided not to implement dynamic expansion” member a minio team
	impossible to add nodes, difficult to add disks, impossible to scale above 16/32 nodes.
	[https://www.minio.io/]



###      -LeoFS
	 is an unstructured object/data storage for the Web and a highly available,
	 distributed, eventually consistent storage system. Amazon S3 compatible, open-source.( written in erlang)
	 More for intern purpose.
      	[https://leo-project.net/leofs/]
      



###      -Quobyte
	turns commodity servers into a Data Center File System. Quobyte delivers linear scalability,
	full fault-tolerance, and lights-out operations so that you can focus on your business
	applications and stop worrying about your storage infrastructure.
	Does not give it price (and don’t seam free, even if opensource?) is mean for powerfull
 	hardware not every on device. Idem than LeoFS Locally managed...
	[https://www.quobyte.com/]


###       -LibStorage
	Libstorage is an open source, platform agnostic, storage provisioning and orchestration framework, model, and API.
       	The libStorage project has been relocated to a subdirectory named libstorage at the root of the project REX-Ray.
	A subtree merge was used in order to retain the original commit history of the libStorage project.
	Efficient but maybe to difficult to install and suport for what it is.
	[https://rexray.readthedocs.io/en/latest/]


###      -Sheepdog
	 is a distributed object storage system for volume and container services and manages the disks and nodes intelligently.
	 Sheepdog features ease of use, simplicity of code and can scale out to thousands of nodes.
	 Is more for admin uses in a company network dont seam enough user-friendly
	[https://sheepdog.github.io/sheepdog/]


###      -Datera
	this is challenging traditional datacenter models, and creating a new data fabric to continuously deliver infrastructure
	in real-time. Easy to use and scale — automated infrastructure that continuously adapts to business needs.
	[https://datera.io/]


###	REX-Ray
	 is an open source, storage management solution designed to support container runtimes such as Docker and Mesos.
	 REX-Ray enables stateful applications, such as databases, to persist and maintain its data after the life cycle of the
	 container has ended. Software, opensource
      	[https://rexray.io/]
      
###	Dell EMC
	It enables digital transformation with trusted solutions for the modern data center.
       DbaaS, [https://www.dellemc.com/en-us/index.htm]
      
###	Robin Cloud Platform (RCP)
	 marshals all your existing commodity hardware resources into a scalable and elastic pool of compute and storage
	resources for Big Data and databases across the data center. Network infrastructure 
	Paying service 
	[https://robinsystems.com/]

###	Diamanti
	 is an appliance built to combine the ease of hyperconverged infrastructure with the unparalleled performance of bare-metal containers.
	… unclear, is not a soft, proivide cloud storage?
	[https://diamanti.com/]

###	NetApp
	 offers storage and data management solutions that enable customers to accelerate business innovations and achieve cost efficiencies.
	is a hybrid cloud data services company Founded in 1992 offers hybrid cloud data services that
 	simplify management of applications and data across cloud and on-premises environments
	[https://www.netapp.com/us/index.aspx]

###	Rook
	Rook is an open source file, block and object storage for your cloud-native environment.
	Is in Alpha
	[https://rook.io/]

###	Hadoop HDFS
	 is a distributed, scalable, and portable filesystem written in Java.(apache)


###	OpenEBS
	is containerized storage for containers integrated tightly into K8S and other environments
	and based on distributed block storage and containerization of storage control.
	OpenEBS is an open source storage platform that provides persistent and containerized 
	block storage for DevOps and container environments. Enterprise service bus (ie middleware?)	(java)
	[https://www.openebs.io/]

###	OpenSDS
	is an open source project established to address integration challenges for Storage Defined Storage (SDS) vendors. (and a cloud storage)
	[https://www.opensds.io/]

###	Springpath
	 is hyperconvergence software that turns standard servers of choice into a single pool of compute and storage resources.
	 in September 22, 2017: Cisco completed the acquisition of Springpath
	(not a product anymore?)

###	StorageOS
	 is a software-based decentralized storage platform designed to provider persistent container storage. Store container on it’s DB?
      	[https://storageos.com/]
      


###	Hedvig
	offers modern software-defined storage for rapidly changing data, apps, and users.
	[https://www.hedvig.io/]

###	Portworx
	 provide a storage solution that spins up quickly and scales elastically based on application requirements,
	 it ‘enable organizations to manage their applications at container speed,
	 in seconds, not days’… software that help to manage containers
      [https://portworx.com/]

###	Pure Storage enterprise
	 all-flash solutions provide the power, reliability, and simplicity you need to tackle the most demanding business and IT problems.
	data flash storage company so I do not put it as a good solution for long cold storage.
	[https://www.purestorage.com/]

###	Infinit
	 allows for the creation of flexible, secure and controlled file storage infrastructure on top of public,
	 private or hybrid cloud resources. An open-source decentralized software-based storage platform for modern environments.
      [https://infinit.sh/]
      
###	-mooseFS,
	 practical and fault tolerant but we will get few suport and it does not suit exactly our
 	needs. (it is a software, not a DbaaS )(is used by reserch lab with petas of data)
	[https://moosefs.com/]

###	-Lustre
	 too much complicated, we don't have a team to manage the filesystem, no enough fault tolerant
	The Lustre® file system is an open-source, parallel file system
	[http://lustre.org/]

###	-ScaleIO,
	 impossible to find, indicate a possible death or lack of support (a it’s a shame, it sound good)
	[https://www.dellemc.com/en-us/storage/data-storage/software-defined-storage.htm#compare0=0]?

###	-storPool,
	 to much sell oriented to be trustworthy 
	is a soft to serelised datacenter I think
	[https://storpool.com/]

###	-DataStax,
	 “Always-On, Distributed Cloud Database
	Built on Apache Cassandra™ and Designed for Hybrid Cloud” profesional oriented
 	(seem production chain oriented to me)
	[https://www.datastax.com/]



###	-Wasabi,
	 cheap cloud storage for profesional as for private person, S3 
	[https://wasabi.com/]







Archiving Amazon S3 Data to Amazon Glacier
[https://aws.amazon.com/blogs/aws/archive-s3-to-glacier/]
This option reduce greatly the price of amazon S3 by using a glacier backup,
the amazon glacier prices apply but the S3 access remain ( with obviously the 4h delay impose by glacier)
the data are at some point (ie: when add and when restored) in double on copy in S3 and one stay in glacier.
This way could be a good solution for an effective use of glacier with a S3 protocol.

[http://blender.ca/aws-glacier-calculator/]
The pricing of glacier is realy low, for 10T (assuming one G by client) keep for 30years and fully recover
it rise to around 50.000 $ or close to 5/6 $ by client (for 30y storage…)
The cost change a latt depending on how hearly we ask for the data, it is 3time this price if ask with only 4h,
but for a 24 or 48 hours periode of recovery.



[https://www.g2crowd.com/categories/runtime]
[https://medium.com/@northxnisha/cloud-native-storage-59624a4fc188]

