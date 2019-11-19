# Lab 6: Connect application to the network

* **Connect with sdk through connection profile**
  * Under the Instantiated Smart Contract, click on `Connect with SDK` from the overflow menu on the right side of the row.
  * Choose from the dropdown for **MSP for connection**, `org1msp`.
  * Choose from **Certificate Authority** dropdown, `Org1 CA`.
  * Download the connection profile by scrolling down and clicking **Download Connection Profile**. This will download the connection json which we will use soon to establish connection.
  * You can click **Close** once the download completes.

![Connect with SDK](.gitbook/assets/sc19.gif)

* **Create an application admin**
  * Go to the **Nodes** tab on the left bar, and under **Certificate Authorities**, choose your organization CA, **Org1 CA**.
  * Click on **Register user**.
  * Give an **Enroll ID** and **Enroll Secret** to administer your application users, `app-admin` and `app-adminpw`.
  * Choose `client` as **Type**.
  * You can leave the **Maximum enrollments** blank.
  * Under **Attributes**, click on **Add attribute**. Give attribute as `hf.Registrar.Roles` = `*`. This will allow this identity to act as registrar and issues identities for our app. Click **Add-attribute**.
  * Click **Register**.

![Application Admin](.gitbook/assets/sc20.gif)

