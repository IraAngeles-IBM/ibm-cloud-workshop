---
description: >-
  Create a custom classifier with Watson Visual Recognition to identify images
  of world cities taken from the ISS
---

# Lab 5 - Identify cities from space



### Summary <a id="summary"></a>

The [Windows on Earth](https://www.windowsonearth.org/) project features images taken by astronauts on the International Space Station. The image galleries include clouds, sunsets, farms, and various world cities at night. This code pattern combines the city images and Watson Visual Recognition to show you how to create a custom classifier that will identify various cities based on their images at night.

### Description <a id="description"></a>

The International Space Station \(ISS\), launched in 1998, serves as a microgravity and space environment research laboratory in which crew members conduct experiments in biology, human biology, physics, astronomy, meteorology, and other fields. These experiments have produced copious amounts of data and experimental results, many of which are available to the public. The Windows on Earth project showcases images taken by astronauts for science research, education, and public outreach. This code pattern uses images of various cities at night to build a visual recognition custom classifier with IBM Watson Visual Recognition, demonstrating how you can use AI to categorize and organize the thousands of images taken from the ISS.

When you have completed this code pattern, you should understand how to:

* Use images from the International Space Station to train a visual recognition custom classifier
* Create a Node.js server that uses the Watson Visual Recognition service for classifying images
* Have a server initialize a visual recognition custom classifier at start-up
* Classify images of cities from space using Watson Visual Recognition

### Flow <a id="flow"></a>

![flow](https://developer.ibm.com/developer/patterns/identify-cities-from-space-using-watson-visual-recognition/images/arch-identify-cities-space.png)

1. The user interacts with the web UI and chooses an image of a city at night, as viewed from space.
2. The image is passed to the server application running in the cloud.
3. The server sends the image to the Watson Visual Recognition service for analysis.
4. The Watson Visual Recognition service classifies the image and returns the information to the server, indicating the confidence level that the image is of a particular city.

### Instructions <a id="instructions"></a>

Find the detailed steps for this pattern in the [README](https://github.com/IBM/cities-from-space/blob/master/README.md). The steps show you how to:

1. Clone the GitHub repository.
2. Create the Watson Visual Recognition service.
3. Add the Watson Visual Recoginition API key to the .env file.
4. Install dependencies and run the server.

