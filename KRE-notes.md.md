
1.  Requirements & Installation (Gus)

Before starting with UI, you need to know some basic concept that we define in order to simplify all the underlying complexity. 

We won't be digging deeper on the technical details and requirements on this presentation in order to focus on all the features of Konstellation. 

From the beginning we've designed our tool as a Cloud Native Application. So it was easy for use to choose Kubernetes as our foundation layer. This gives us lots of advantages out-of-the-box, cloud vendor agnostic, easy orchestration, distribution, monitoring, and lot more.

So is enough to say that if you have a working Kubernetes cluster and a user with the proper permissions, you are able to install and run all this right away, just deploying it with a few commands, thanks to the helm chart that we've created. (helm is how you package Kubernetes apps).

Any Kubernetes means that you can use your local machine, a bare metal cluster or any cloud flavor of Kubernetes (Google, Amazon or Azure).


2.  Use case implementation (Gus)

Starting from top to bottom we have the following abstractions:


- **Konstellation Runtime Engine:** 
	This is the central component that acts as an operation tool to create and manage all the needed resources for each solution that you would like to put in production. This includes an UI and a backend. It's the only piece that is created on installation.

- **Runtime:**
This is an environment that isolated from all other runtimes and other resources. Its where our price estimation solution is going to run. 

This two concepts alone provides flexibility. You can decide to have one engine per each of your clients. Or for a smaller company just a single engine with a runtime per client. Up to you.

**- Version:**
A version is all the software components and models on a given point in time. This is an important idea for us, if you make any change at any level, model or code, you have a new version that would be deployed. Hence, that you can have multiple versions of your solution deployed within the same runtime.

**- KRT:** 
¿And how you create and deploy your version? You create a KRT file. This is just a package that contains the definition of your solution, and also the code and the model to be deployed and ran on your runtime.

Currently this file is generated manually, but in future versions this will be exported by a Data Scientist from the Konstellation Development Toolkit directly. 


3.  GO TO ADMIN UI

- Initial screen
	- Explain runtime list, and navigation

- Version screen
	- Add version
	- List version with current status

- Explain status
	- STOPPED: No resource is actually running (no resources in use)
	- STARTED: All needed resources are running, but not accessible
	- PUBLISHED: All is running AND accessible to consume.

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
eyJoaXN0b3J5IjpbLTIxMzIzODk1MDQsLTE1NDkzMjU1MiwtMj
AyNzk3NTkxN119
-->