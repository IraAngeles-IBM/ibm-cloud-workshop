# Lab 2 - Forest Fire Detection Using Visual Recognition

## Fire Alarm using Watson Visual Recognition

This project is a how-to guide on using Watson Visual Recognition service to analyse an image and based on a trigger word then send a event command to IoT Device.In this example node-red is used to create an image upload form which sends the image to Watson Visual Recognition and trigger an IoT device whenever fire is detected in the image. [Click here to try what we're going to build.](https://nodered-iotimageanalysis001.mybluemix.net/upload)

## NOTE: Please check the Video Tutorial at the bottom of the page if you face any issues! 

1. Login/signup in to your [IBM Cloud Account](https://ibm.biz/BdYtcs)

2. Go to Catalog and create the following services:

* \*\*\*\*[**Internet of Things Platform Starter**](https://cloud.ibm.com/catalog/starters/internet-of-things-platform-starter)\*\*\*\*

\(Alternatively, You can browse through IBM Cloud's Catalog &gt; Starter Kits &gt; Internet of Things Platform Starter\)

     - Input the App Name, in this example, use "NodeRed-IotImageAnalysis" and click create button.  \(Please suffix the App Name with your desired 4 random numbers\)

![](.gitbook/assets/image%20%2814%29.png)

    - While IBM Cloud creating the Cloud Foundry App for you, we can monitor its status from the [resource dashboard](https://cloud.ibm.com/resources) . Once we see the App is up running, click on the app and a new window will pop on the right hand side. 

![The application link is provided at section - Routes. Open a new tab by right-clicking on the Route&apos;s link. ](.gitbook/assets/image%20%2842%29.png)

![The route&apos;s link is your application, now we shall activate it. The following screen is the first step, click Next](.gitbook/assets/image%20%2839%29.png)

![On the 2nd screen, select the second option and ensure that you&apos;ve checked the only option there.](.gitbook/assets/image%20%2838%29.png)

![The 3rd screen, click next](.gitbook/assets/image%20%2820%29.png)

![The 4th screen confirm the creation of Node-Red App.](.gitbook/assets/image%20%2817%29.png)

![Once the Node-RED is activated, Click to open the Node-RED Flow Editor](.gitbook/assets/image%20%2840%29.png)

![Here the Node-RED Flow editor. We leave this editor tab open at the moment and we shall come back after we have activated the Watson&apos;s AI Services. ](.gitbook/assets/image%20%2822%29.png)

* [Visual Recognition](https://cloud.ibm.com/catalog/services/visual-recognition)

\(Alternatively, You can browse through IBM Cloud's Catalog &gt; AI &gt; Visual Recognition\)

![Create a Visual Recognition service.](.gitbook/assets/image%20%2824%29.png)

![After the Visual Recognition Service created, we shall create a new Service Credential.](.gitbook/assets/image%20%2847%29.png)

![&#xE4B;&#xE35;Leave everything by default and click &apos;Add&apos;.](.gitbook/assets/image%20%284%29.png)

![The new Service Credential is created and we shall obtain the API key from here and use for Node-RED.](.gitbook/assets/image%20%287%29.png)

At this point, 2 services have been created, next step is to link these 2 services by using the API Key generated and the JSON file which is available on [github](https://github.com/krishnac7/IotImageAnalysis).

![Open the flow.JSON file in the text editor.](.gitbook/assets/image%20%288%29.png)

Now, go back to Node-RED Flow that we leave it open.

![Click on the Menu &amp;gt; Import &amp;gt; Clipboard](.gitbook/assets/image%20%286%29.png)

![Copy the code from flows.JSON and paste the source code \(copied from flows.JSON\) here and click &apos;Import&apos; button.](.gitbook/assets/image%20%2821%29.png)

![The Node-RED Modules have been imported. Double click on the Visual Recognition. ](.gitbook/assets/image.png)

![Ensure that the the correct Service Endpoint is selected, next, use the API Key from a new service credential created from previous step, and input here and click &apos;Done&apos;.](.gitbook/assets/image%20%2837%29.png)

![Click on &apos;Deploy&apos; button.](.gitbook/assets/image%20%2827%29.png)

Now, the 2 services are linked and up running and it's time to run the application. Back to IBM's Catalog and look for Cloud Foundry App which has been created at the first step. Look for Route's link, It may look like   
  
[https://nodered-iotimageanalysis001.mybluemix.net](https://nodered-iotimageanalysis001.mybluemix.net)

In order to run the application, please suffix the Route's URL with "/upload".

![](.gitbook/assets/image%20%2815%29.png)

![Give a try to upload a photo and see the result.](.gitbook/assets/image%20%2836%29.png)

### Please use the [Video Tutorial](https://github.com/krishnac7/Media/blob/master/IotImageAnalysis/imageAnalysisIot.mp4) if you still have problem troubleshooting! 

#### Github repository:  [https://github.com/krishnac7/IotImageAnalysis](https://github.com/krishnac7/IotImageAnalysis)

Useful link : IBM Code Pattern - [https://developer.ibm.com/patterns](https://developer.ibm.com/patterns)

