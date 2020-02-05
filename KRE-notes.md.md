
1.  Requirements & Installation (Gus)

Before showing the app, I will tell you about some basic concept that we defined in order to simplify all the underlying complexity. 

Today we won't stop much on the technical details and requirements in order to focus on the main features of Konstellation. 

From the beginning we've designed our tool as a Cloud Native Application. So it was easy to pick Kubernetes as our foundation layer. This alone gives us lots of advantages out-of-the-box, cloud vendor agnostic, easy orchestration, distribution, monitoring, and lot more.

Basically that's the main requirement. If you have a Kubernetes cluster and a user with the proper permissions, you can install and run all this right now with a few commands. You can get the helm chart that we provide and you are good to go. (helm is how you package Kubernetes apps).

And of course, being a Kubernetes application, it means that you can run it in your local machine, a bare metal cluster or any cloud flavor of Kubernetes (Google, Amazon or Azure).


2.  Use case implementation (Gus)

On top of that base layer that is kubernetes we have creayed awith our own abstractions, trying to cover all the complexity behind more simple concepts.


**Konstellation Runtime Engine** 
	This is the central component that acts as an operation tool to create and manage all the resources associated with each solution that you would put in production. It's created on installation, it includes an UI, an API some other components.

 **Runtime**
Is an environment that is isolated from all other runtimes and other resources. This is  where you can put one or more solutions. Things inside a runtime will share resources. Here is where our price estimation solution is going to run. 

This two concepts alone provides great flexibility. You can decide to have one engine per client. Or for a smaller company just a single engine with a runtime per client. Up to your needs.

**Version**
A version is the sum of all the code and models that make your solution work. This is an important idea for us, if you make changes at any level, model or code, you have a new version that must be uploaded. This make versions inmutable entities. Easier to track over time and debug. You can have multiple versions of your solution running within the same runtime.

**KRT** 
¿And how do you create and put your version in a runtime? You need a KRT file. This is a package that contains a version. Inside this package you put the code, the model and a definition file of your solution. This is the file that you can upload to a runtime and would become resources at some point.

A side note. At this point the KRT file is generated manually, but in future versions this will be exported by a Data Scientist from the Konstellation Development Toolkit directly. 

3.  GO TO ADMIN UI

- Initial screen
Here you have a view of all the runtimes, and you can create more.

- Version screen
Once you choose a runtime, you see all it's version and the status of each one. Also add new ones. Let's upload one now.

- Explain status
	- **STOPPED**: No resource is actually running (no resources in use)
	- **STARTED**: All needed resources are running, but not accessible
	- **PUBLISHED**: All is running AND accessible to consume.

- Show it cannot be started until is configured
	- This is important to separate code from the environment configuration.

- Version Status screen
	- Here you can see the version and its components status in a more visual way.
	- Here you have complete control over this version. 

- Start & publish
	- To change status you can click START and then PUBLISH
	- Now that it is published the version is accessible from the Internet.

- Show APP and make a call to prediction




<!--stackedit_data:
eyJoaXN0b3J5IjpbMTI3NjU3OTc1MywxMDYyMTM5MjczLC05OT
g4NjMyNDcsLTIxMjA0MDg4MjAsMTYxMjI3NjEzOCwxOTI4Mjkz
Njc2LC0xOTgyMDI5MjAsNzk0OTgxMDc3LC04NDUwNjUzNzgsLT
g4MjQzMjUwMywtMTc4OTUwMDM3OSwtMTAxMTg1MzQ0MSwtMjA0
MTAxNzEwMywxNjk0MzMwMTA1LDE4OTczMjE5NzQsMTUxNjU0Mj
Q0Niw0NzI5MDAzODksLTE0NTAzODc3NTUsLTcxNjM4NTE3LDEx
ODUyNDEwNDBdfQ==
-->