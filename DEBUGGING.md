Troubleshooting
===============

Jupyter Notebooks
-----------------

* Make sure the pip install ran correctly. You might need to restart the kernel and run the cells from the top after the pip install runs the first time.
* Many of the cells rely on variables that are set in earlier cells. Some of these are cleared in later cells. Start over at the top when troubleshooting.
* Many of the cells rely on service credentials from Bluemix that are set in earlier cells. Make sure to add your service credentials correctly.  
* If the Start Websocket client step throws an error as shown below, please refer to the step `Update the websocket URL in the notebook` in Section 10 of the documentation.

          --- response header ---
          HTTP/1.1 500 Error 
          X-Backside-Transport: FAIL FAIL
          Content-Type: text/xml
          Connection: close
          
Node-RED
--------

* Refer to sections 5 & 6 in the documentation regarding the usage of Node-RED flow. Please make sure to update the Node-RED based URL in the json file before importing it into the Node-RED editor.

Watson Conversation
--------

* Make sure that the Watson Conversation service credentials which had been noted down in step 2 and and Workspace ID which had been noted down in step 3, has been updated in the Watson Conversation node in Node Red Flow according to step 5. 
