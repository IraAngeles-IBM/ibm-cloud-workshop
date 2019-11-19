# Lab 4: FabCar Blockchain Sample - Build a Network

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

* **Use your CA to register identities**
  * Select the **Org 1 CA** Certificate Authority that we created.
  * First, we will register an admin for our organization "org1". Click on the **Register User** button. Give an **Enroll ID** of `org1admin`, and **Enroll Secret** of `org1adminpw`. Click **Next**. Set the **Type** for this identity as `client` and select from any of the affiliated organizations from the drop-down list. We will leave the **Maximum enrollments** and **Add Attributes** fields blank.
  * We will repeat the process to create an identity of the peer. Click on the **Register User** button. Give an **Enroll ID** of `peer1`, and **Enroll Secret** of `peer1pw`. Click **Next**. Set the **Type** for this identity as `peer` and select from any of the affiliated organizations from the drop-down list. We will leave the **Maximum enrollments** and **Add Attributes** fields blank.

![client](../.gitbook/assets/sc6.gif)

![peer](../.gitbook/assets/sc7.gif)

* **Create the peer organization MSP definition**
  * Navigate to the **Organizations** tab in the left navigation and click **Create MSP definition**.
  * Enter the **MSP Display name** as `Org1 MSP` and an **MSP ID** of `org1msp`.
  * Under **Root Certificate Authority** details, specify the peer CA that we created `Org1 CA` as the root CA for the organization.
  * Give the **Enroll ID** and **Enroll secret** for your organization admin, `org1admin` and `org1adminpw`. Then, give the Identity name, `Org1 Admin`.
  * Click the **Generate** button to enroll this identity as the admin of your organization and export the identity to the wallet. Click **Export** to export the admin certificates to your file system. Finally click **Create MSP definition**.

![](../.gitbook/assets/sc8.gif)



* **Create a peer**
  * On the **Nodes** page, click **Add peer**.
  * Click **IBM Cloud** under Create a new peer and **Next**.
  * Give your peer a **Display name** of `Peer Org1`.
  * On the next screen, select `Org1 CA` as your **Certificate Authority**. Then, give the **Enroll ID** and **Enroll secret** for the peer identity that you created for your peer, `peer1`, and `peer1pw`. Then, select the **Administrator Certificate \(from MSP\)**, `Org1 MSP`, from the drop-down list and click **Next**.
  * Give the **TLS Enroll ID**, `admin`, and **TLS Enroll secret**, `adminpw`, the same values are the Enroll ID and Enroll secret that you gave when creating the CA. Leave the **TLS CSR hostname** blank.
  * The last side panel will ask you to **Associate an identity** and make it the admin of your peer. Select your peer admin identity `Org1 Admin`.
  * Review the summary and click **Submit**.

![Create Peer](../.gitbook/assets/sc9.gif)

