# Lab 4: FabCar Blockchain Sample - Build Network

## Structure of the Network

![Sample basic network structure](../.gitbook/assets/image%20%2824%29.png)

We will build a network as provided by the IBM Blockchain Platform [documentation](https://console.bluemix.net/docs/services/blockchain/howto/ibp-console-build-network.html#ibp-console-build-network). This will include creating a channel with a single peer organization with its own MSP and CA \(Certificate Authority\), and an orderer organization with its own MSP and CA. We will create the respective identities to deploy peers and operate nodes.



### Create your organization and your entry point to your blockchain

* **Create your peer organization CA**
  * Click **Add Certificate Authority**.
  * Click **IBM Cloud** under **Create Certificate Authority** and **Next**.
  * Give it a **Display name** of `Org1 CA`.
  * Specify an **Admin ID** of `admin` and **Admin Secret** of `adminpw`.

![](../.gitbook/assets/sc5.gif)



