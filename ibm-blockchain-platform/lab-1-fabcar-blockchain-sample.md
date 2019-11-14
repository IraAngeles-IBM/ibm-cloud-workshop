# Lab 2: FabCar Blockchain Sample - Overview

This code pattern demonstrates setting up a network on the IBM Blockchain Platform and deploying the Fabcar smart contract on the network. Next, we setup our application to interact with the network including identities to submit transactions on the smart contract. The application is setup with a Node.js server using the Fabric Node SDK to process requests to the network, and an Angular client to bring up a web interface.

When the reader has completed this code pattern, they will understand how to:

* Setup a Hyperledger Fabric network on IBM Blockchain Platform
* Install and instantiate smart contract through the IBM Blockchain Platform
* Develop a Node.js server with the Hyperledger Fabric SDK to interact with the deployed network
* Create an Angular frontend for the web app to interface with the network

## Architecture flow

![](../.gitbook/assets/image%20%2825%29.png)



The developer uses the IBM Blockchain Platform Extension for VS Code to:

1. The Blockchain Operator sets up the IBM Blockchain Platform service
2. The IBM Blockchain Platform enables to create a Hyperledger Fabric network onto a IBM Kubernetes Service, allowing to install and instantiate the Fabcar smart contract on the network
3. The Node.js application server uses the Fabric sdk to interact with the deployed network on IBM Blockchain Platform and creates APIs for a web client
4. The Angular client uses the Node.js application API to interact with the network
5. The User interacts with the Fabcar Angular web interface to update and query the blockchain ledger and state

## Included components

* [IBM Blockchain Platform](https://console.bluemix.net/docs/services/blockchain/howto/ibp-v2-deploy-iks.html#ibp-v2-deploy-iks) gives you total control of your blockchain network with a user interface that can simplify and accelerate your journey to deploy and manage blockchain components on the IBM Cloud Kubernetes Service.
* [IBM Cloud Kubernetes Service](https://www.ibm.com/cloud/container-service) creates a cluster of compute hosts and deploys highly available containers. A Kubernetes cluster lets you securely manage the resources that you need to quickly deploy, update, and scale applications.
* [IBM Blockchain Platform Extension for VS Code](https://marketplace.visualstudio.com/items?itemName=IBMBlockchain.ibm-blockchain-platform) is designed to assist users in developing, testing, and deploying smart contracts -- including connecting to Hyperledger Fabric environments.

### Featured technologies

* [Hyperledger Fabric v1.4](https://hyperledger-fabric.readthedocs.io/) is a platform for distributed ledger solutions, underpinned by a modular architecture that delivers high degrees of confidentiality, resiliency, flexibility, and scalability.
* [Node.js](https://nodejs.org/) is an open source, cross-platform JavaScript run-time environment that executes server-side JavaScript code.
* [Express.js](https://expressjs.com/) is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.
* [Angular.io](https://angular.io/) is a front-end framework for building web applications.

#### Steps

> To run a local network, you can find steps [here](https://github.com/IBM/fabcar-blockchain-sample/blob/master/docs/run-local.md)

1. [Clone the repo](https://github.com/IBM/fabcar-blockchain-sample/blob/master/README.md#1-clone-the-repo)
2. [Package the smart contract](https://github.com/IBM/fabcar-blockchain-sample/blob/master/README.md#2-package-the-smart-contract)
3. [Create IBM Cloud services](https://github.com/IBM/fabcar-blockchain-sample/blob/master/README.md#3-create-ibm-cloud-services)
4. [Build a network](https://github.com/IBM/fabcar-blockchain-sample/blob/master/README.md#4-build-a-network)
5. [Deploy FabCar Smart Contract on the network](https://github.com/IBM/fabcar-blockchain-sample/blob/master/README.md#5-deploy-fabcar-smart-contract-on-the-network)
6. [Connect application to the network](https://github.com/IBM/fabcar-blockchain-sample/blob/master/README.md#6-connect-application-to-the-network)
7. [Run the application](https://github.com/IBM/fabcar-blockchain-sample/blob/master/README.md#7-run-the-application)

