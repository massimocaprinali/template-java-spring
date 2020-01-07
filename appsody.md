# Appsody

This guide shows you how to enable appsody in your template.

## Enabling appsody

- Go to the project directory.

- Initialize Appsody without using a template on the existing project.

```
appsody init <stack> none
```

- Since ours is a springboot application, let us use one of the existing stacks from appsody.

- To get the list of appsody stacks, run the below command.

```
appsody list
```

You will get to see something like below.

```
┌$ appsody list

REPO                 	ID                       	VERSION  	TEMPLATES                       	DESCRIPTION
experimental-index   	java-spring-boot2-liberty	0.1.9    	*default                        	Spring Boot on Open Liberty & OpenJ9 using Maven
experimental-index   	mystack                  	0.1.0    	*hello                          	sample stack to help creation of more appsody stacks
experimental-index   	nodejs-functions         	0.1.3    	*simple                         	Serverless runtime for Node.js functions
experimental-index   	quarkus                  	0.1.5    	*default                        	Quarkus runtime for running Java applications
experimental-index   	vertx                    	0.1.2    	*default                        	Eclipse Vert.x runtime for running Java applications
incubator-index      	java-microprofile        	0.2.14   	*default                        	Eclipse MicroProfile on Open Liberty & OpenJ9 using Maven
incubator-index      	java-spring-boot2        	0.3.14   	*default, kotlin                	Spring Boot using OpenJ9 and Maven
incubator-index      	nodejs                   	0.2.5    	*simple                         	Runtime for Node.js applications
incubator-index      	nodejs-express           	0.2.6    	*simple, simple-sample, skaffold	Express web framework for Node.js
incubator-index      	nodejs-loopback          	0.1.4    	*scaffold                       	LoopBack 4 API Framework for Node.js
incubator-index      	python-flask             	0.1.3    	*simple                         	Flask web Framework for Python
incubator-index      	swift                    	0.1.4    	*simple                         	Runtime for Swift applications
incubator-index-local	nodejs-express           	0.2.6    	*simple, simple-sample, skaffold	Express web framework for Node.js
```

- Now let us enable our existing project using the existing appsody springboot stack as follows.

```
appsody init incubator-index/java-spring-boot2  none
```

- To test the project, run the below command.

```
appsody test
```

- To build the project, run the below command.

```
appsody build
```

- To run the project, run the below command.

```
appsody run
```

- To stop the application, run the below command.

```
appsody stop
```

- If you want to deploy the application to a kubernetes cluster or openshift, you need a deployment manifest. In order to generate it, run the below command.

```
appsody deploy --generate-only
```
