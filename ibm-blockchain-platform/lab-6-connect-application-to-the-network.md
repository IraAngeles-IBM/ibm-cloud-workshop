# Lab 6: Connect application to the network

* **Connect with sdk through connection profile**
  * Under the Instantiated Smart Contract, click on `Connect with SDK` from the overflow menu on the right side of the row.
  * Choose from the dropdown for **MSP for connection**, `org1msp`.
  * Choose from **Certificate Authority** dropdown, `Org1 CA`.
  * Download the connection profile by scrolling down and clicking **Download Connection Profile**. This will download the connection json which we will use soon to establish connection.
  * You can click **Close** once the download completes.

![Connect with SDK](../.gitbook/assets/sc19.gif)

* **Create an application admin**
  * Go to the **Nodes** tab on the left bar, and under **Certificate Authorities**, choose your organization CA, **Org1 CA**.
  * Click on **Register user**.
  * Give an **Enroll ID** and **Enroll Secret** to administer your application users, `app-admin` and `app-adminpw`.
  * Choose `client` as **Type**.
  * You can leave the **Maximum enrollments** blank.
  * Under **Attributes**, click on **Add attribute**. Give attribute as `hf.Registrar.Roles` = `*`. This will allow this identity to act as registrar and issues identities for our app. Click **Add-attribute**.
  * Click **Register**.

![Application Admin](../.gitbook/assets/sc20.gif)

* **Update application connection**
  * Copy the connection profile you downloaded into [server folder](https://github.com/IBM/fabcar-blockchain-sample/blob/master/web-app/server)
  * Update the [config.json](https://github.com/IBM/fabcar-blockchain-sample/blob/master/web-app/server/config.json) file with:
    * The connection json file name you downloaded.
    * The **enroll id** and **enroll secret** for your app admin, which we earlier provided as `app-admin` and `app-adminpw`.
    * The orgMSP ID, which we provided as `org1msp`.
    * The caName, which can be found in your connection json file under "organization" -&gt; "org1msp" -&gt; certificateAuthorities". This would be like an IP address and a port.
    * The username you would like to register.
    * Update gateway discovery to `{ enabled: true, asLocalhost: false }` to connect to IBP.

> the current default setup is to connect to a local fabric instance from VS Code

```text
{
    "connection_file": "mychannel_fabcar_profile.json",
    "appAdmin": "app-admin",
    "appAdminSecret": "app-adminpw",
    "orgMSPID": "org1msp",
    "caName": "184.173.1.18:31317",
    "userName": "user1",
    "gatewayDiscovery": { "enabled": true, "asLocalhost": false }
}
```

