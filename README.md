# watson-nao-robot


This journey takes you through end to end flow of steps in building an interactive interface between NAO Robot and Watson Conversation API. Nao Robot listen the vocal query and converts it into text and sends it to Node Red Flow. The Node Red Flow uses Watson Conversation API to break and map the text into intents and entities for which it has been trained already. The conversation API through Node Red Flow further linked to a Jupyter Notebook in Data Science Experience(DSX). In this notebook statistical analysis is performed on the finantial data set. The result of the query is now again sent back to Node Red Flow. Which is transfered to Nao Robo and it speaks the result.



![](doc/source/images/Robot_Architecture_Diagram.png)

1. The user asks the specific questions to the Robot.
2. Robot will convert the speech into text and it will send the text to Node Red Flow.
3. The Node Red Flow uses the Watson Conversation API for handling the text and web socket for transferring the input and output between Node Red Flow and Jupyter notebook. 
4. The Watson Conversation API takes the text input in the form of natural language and breaks and maps it to intents and entities for which it has been trained for.
5. The context of the conversation is saved to the Cloudant DB so that the Conversation API is able to save the state and track the conversation flow of the user.
6. The data is stored in the Object storage.
7. Data is utilized as csv files.
8. The Jupyter notebook processes the data and generates insights.
9. The Jypyter notebook is powered by Spark.


## Included components

* [Node-RED](https://console.bluemix.net/catalog/starters/node-red-starter): Node-RED is a programming tool for wiring together APIs and online services.

* [IBM Data Science Experience](https://www.ibm.com/bs-en/marketplace/data-science-experience): Analyze data using RStudio, Jupyter, and Python in a configured, collaborative environment that includes IBM value-adds, such as managed Spark.

* [Bluemix Object Storage](https://console.ng.bluemix.net/catalog/services/object-storage/?cm_sp=dw-bluemix-_-code-_-devcenter): A Bluemix service that provides an unstructured cloud data store to build and deliver cost effective apps and services with high reliability and fast speed to market.

## Featured technologies

* [Jupyter Notebooks](http://jupyter.org/): An open-source web application that allows you to create and share documents that contain live code, equations, visualizations and explanatory text.


# Steps

Follow these steps to setup and run this developer journey. The steps are
described in detail below.

1. [Sign up for the Data Science Experience](#1-sign-up-for-the-data-science-experience)
2. [Create Bluemix services](#2-create-bluemix-services)
3. [Import the Node-RED flow](#3-import-the-node-red-flow)
4. [Note the websocket URL](#4-note-the-websocket-url)
5. [Update the websocket URL](#5-update-the-websocket-url)
6. [Create the notebook](#6-create-the-notebook)
7. [Add the data](#7-add-the-data)
8. [Update the notebook with service credentials](#8-update-the-notebook-with-service-credentials)
9. [Run the notebook](#9-run-the-notebook)
10.[Push the results back to websocket](#10-Push the results back to web socket)

## 

