# Lab 5: FabCar Blockchain Sample - Build a Network \(2/3\)

### Create the node that orders transactions

* **Create your orderer organization CA**
  * Click **Add Certificate Authority**.
  * Click **IBM Cloud** under **Create Certificate Authority** and **Next**.
  * Give it a unique **Display name** of `Orderer CA`.
  * Specify an **Admin ID** of `admin` and **Admin Secret** of `adminpw`.

![](../.gitbook/assets/sc10.gif)

* **Use your CA to register orderer and orderer admin identities**
  * In the **Nodes** tab, select the **Orderer CA** Certificate Authority that we created.
  * First, we will register an admin for our organization. Click on the **Register User** button. Give an **Enroll ID** of `ordereradmin`, and **Enroll Secret** of `ordereradminpw`. Click **Next**. Set the **Type** for this identity as `client` and select from any of the affiliated organizations from the drop-down list. We will leave the **Maximum enrollments** and **Add Attributes** fields blank.
  * We will repeat the process to create an identity of the orderer. Click on the **Register User** button. Give an **Enroll ID** of `orderer1`, and **Enroll Secret** of `orderer1pw`. Click **Next**. Set the **Type** for this identity as `peer` and select from any of the affiliated organizations from the drop-down list. We will leave the **Maximum enrollments** and **Add Attributes** fields blank.

![](../.gitbook/assets/sc11.gif)

