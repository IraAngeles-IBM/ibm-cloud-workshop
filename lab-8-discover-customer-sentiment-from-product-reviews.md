---
description: 'https://ws-dis-food-reviews.mybluemix.net/'
---

# Lab 8 - Discover customer sentiment from product reviews

### Summary <a id="summary"></a>

Do you know what your customers really think about your product or service? Knowing this information is vital to your business and livelihood and lets you adapt your business as needed. This code pattern uses food reviews to explain how to easily extract insights from raw review data. It walks you through a working example of a web application that queries and manipulates data from Watson Discovery. And, with the aid of custom models using Watson Knowledge Studio, the data has additional enrichments that provide improved insights for user analysis.

### Description <a id="description"></a>

Rather than relying on your own assumptions, how can you be sure what exactly your customers are saying about your business? The answer is in being able to analyze raw customer feedback in reviews, forums, and so on. Through the use of various UI components, the Node.js app in this code pattern demonstrates how to extract and visualize enriched data provided by the Watson Discovery engine. The data is further enhanced by a custom-built Watson Knowledge Studio model created specifically for handling food review type data. You can use the multiple UI components in this app as a starting point for developing your own Watson Discovery applications.

As you learned in previous code patterns, the main benefit of using Watson Discovery is its powerful engine that provides cognitive enrichments and insights into your data. The app in this code pattern provides examples of how to showcase these enrichments through the use of filters, lists, and graphs.

With Watson Knowledge Studio, you can teach Watson about additional entities and relationships that go beyond its default entity extraction and enrichment process with a custom annotation model. Through the use of annotations, you can indicate entities and entity relationships on a small subset of documents, which can then be applied to a much larger set of similar documents. This model can then be applied to a Watson Discovery instance and incorporated into the Discovery enrichment process as documents are uploaded into the service.

When you have completed this code pattern, you should know how to:

* Load and enrich data in Watson Discovery
* Use Watson Knowledge Studio to create a custom annotation model
* Deploy a Watson Knowledge Studio model to Discovery
* Query and manipulate data in Discovery
* Create UI components to represent enriched data created by Discovery
* Build a complete web app that uses JavaScript technologies to feature Discovery data and enrichments

### Flow <a id="flow"></a>

![customer-insights-food-reviews](https://developer.ibm.com/developer/patterns/get-customer-insights-from-product-reviews/images/food-reviews.png)

1. Import the customer reviews into the Discovery collection.
2. Load a sample set of review documents into Watson Knowledge Studio for annotation.
3. Create a Watson Knowledge Studio model and train the model.
4. Deploy the Watson Knowledge Studio model to a Watson Discovery instance.
5. The user interacts with the back-end server through the app UI. The front-end app UI uses React to render search results and can reuse all of the views that the back end uses for server-side rendering. The front end uses semantic-ui-react components and is responsive.
6. Process user input and route it to the back-end server, which is responsible for server-side rendering of the views to be displayed on the browser. The back-end server is written using Express and uses the express-react-views engine to render views written using React.
7. The back-end server sends the user requests to Watson Discovery. It acts as a proxy server, forwarding queries from the front end to the Discovery API while keeping sensitive API keys concealed from the user.

### Instructions <a id="instructions"></a>

Ready to put this code pattern to use? Complete details on how to get started running and using this application are in the [README](https://github.com/IBM/watson-discovery-food-reviews/blob/master/README.md).

### Conclusion <a id="conclusion"></a>

This code pattern shows how you can use food reviews to explain how to easily extract insights from raw review data. The code pattern is part of the [Learning Path: Getting started with Watson Discovery](https://developer.ibm.com/series/learning-path-watson-discovery) series. To continue the series and learn about more Watson Discovery Service features, take a look at the next code pattern, [Enhance customer helpdesk with Smart Document Understanding](https://developer.ibm.com/patterns/enhance-customer-help-desk-with-smart-document-understanding).

## Notes

things to take note 

1. make sure that the api-key, model ids and environment id are correctly retrieved from watson-discovery service.
2. make sure that the env.sample is the right place to be updated, then copy it to new file which is ".env"
3. file - package.json need to have a unique service's name, its located at line number 2
4. file - package.json at line number 45, use this -&gt; "node": "8.9.4" as the stable node version on IBM Cloud Foundry.
5. IBM Cloud Deployment : this app might consume a lot of memory, so recommend to set it at least 512mb, but it works better with 2gb of memory allocated. Take a look at file - manifest.yml as below. The name of this application should also match to service name specified in package.json from 4\)

```text
---
applications:
- path: .
  name: ws-dis-food-reviews
  buildpack: sdk-for-nodejs
  memory: 2048M
  random-route: false
  instances: 1
```

## Troubleshooting

* Error when loading files into Discovery

  > Loading all 1000 document files at one time into Discovery can sometimes lead to "busy" errors. If this occurs, start over and load a small number of files at a time.

* No keywords appear in the app

  > This can be due to not having a proper configuration file assigned to your data collection. See [Step 5](https://github.com/IBM/watson-discovery-food-reviews#5-import-corpus-documents) above.

