---
description: 'https://watson-banking-chatbot-23o235i432t2-4t9485052.mybluemix.net/'
---

# Lab 9 - Create a banking chatbot

### Summary <a id="summary"></a>

Built for developers familiar with JavaScript and Node.js interested in making a web UI chatbot with artificial intelligence abilities, this code pattern uses the IBM Watson Node.js SDK to include conversation interaction, anger detection, natural language understanding, and answer discovery. Answers are discovered from a collection of FAQ documents. Built as a fictional financial institution, this app calls out to simple banking services code as an example of how to include external business data in a conversation response.

### Description <a id="description"></a>

In this pattern, you create a chatbot using Node.js and IBM Watson Assistant. The flow is enhanced by using Watson Natural Language Understanding to identify entities and Watson Tone Analyzer to detect customer emotions. For FAQs, a call to the Watson Discovery service uses passage retrieval to pull answers from a collection of documents.

When you complete this pattern, you will understand how to:

* Create a chatbot that converses through a web UI using Watson Assistant and Node.js
* Use Watson Discovery with passage retrieval to find answers in FAQ documents
* Use Watson Tone Analyzer to detect emotion in a conversation
* Identify entities with Watson Natural Language Understanding

### Flow <a id="flow"></a>

![create banking chatbot flow chart](https://developer.ibm.com/developer/patterns/create-cognitive-banking-chatbot/images/Create-a-banking-chatbot.png)

1. The FAQ documents are added to the Watson Discovery collection.
2. The user interacts with a chatbot through the app UI.
3. User input is processed with Tone Analyzer to detect anger. An anger score is added to the context.
4. User input is processed with Natural Language Understanding. The context is enriched with detected entities and keywords \(for example, a location\).
5. The input and enriched context is sent to Watson Assistant, which recognizes intent, entities, and dialog paths. It responds with a reply, an action, or both.
6. Optionally, a requested action is performed by the app. This action might include looking up additional information from bank services to append to the reply or using Discovery to reply with an answer from the FAQ documents.

### Instructions <a id="instructions"></a>

Ready to put this code pattern to use? Complete details on how to get started running and using this application are in the [README.md](https://github.com/IBM/watson-banking-chatbot/blob/master/README.md) file.

### Conclusion <a id="conclusion"></a>

This code pattern showed how you can use the IBM Watson Node.js SDK to include conversation interaction, anger detection, natural language understanding, and answer discovery in a banking chatbot. The code pattern is part of the [Watson Assistant learning path](https://developer.ibm.com/series/learning-path-watson-assistant/). To continue the learning and learn about more Watson Assistant features, take a look at the next code pattern, [Create a Google Action with Watson Assistant](https://developer.ibm.com/patterns/create-an-agent-for-rental-car-reservations/).

### Notes <a id="conclusion"></a>

1. It works perfectly on free tier or lite plan account.
2. Ensure that all Watson services are created prior to deployment on node.js application.
3. Upload document to Watson, for the five documents, please upload it one by one.
4. Cloud deployment, please edit the manifest.yml to as the following \(Note that, the name of the application can be any, but it has to be unqiue across cloud foundry app\).
5. Cloud deployment, please edit package.json for the node.js app engine version number to "node": "8.9.4"

{% code title="Manifest.yml" %}
```text
---
applications:
- path: .
  memory: 256M
  instances: 1
  name: watson-banking-chatbot-23o235i432t2-4t9485052
  random-route: false
  buildpack: sdk-for-nodejs
```
{% endcode %}

{% code title="package.json" %}
```text
  "repository": "github:IBM/watson-banking-chatbot",
  "engines": {
    "node": "8.9.4"
  },
```
{% endcode %}

