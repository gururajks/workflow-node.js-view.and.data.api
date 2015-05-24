# Autodesk View and Data API Node.js Basic Sample


[![build status](https://api.travis-ci.org/Developer-Autodesk/workflow-node.js-view.and.data.api.png)](https://travis-ci.org/Developer-Autodesk/workflow-node.js-view.and.data.api)




## Description
A sample demonstrating how to view a model in a web application with the Autodesk View & Data API. This web application has a basic Node.js 
server and JavaScript/HTML5 client. This sample does not demonstrate how to upload a model to the Autodesk server for translation. See instructions below 
to prepare a model to be consumed in this sample.


## Dependencies
Install Node.js on your machine and clone this repo. Download the project dependencies using npm before running the app by running 
the following command in the project root directory
```
npm install
```
on the node.js console. This will install the following node.js modules in the project:
- express
- request
- serve-favicon

This sample does not include the workflow of uploading models. on the server It depends on other workflow samples to upload models and 
get model URNs - as explained in the Setup/Usage Instructions.


## Setup/Usage Instructions
 
* Apply for your own credentials (API keys) from [http://developer.autodesk.com](http://developer.autodesk.com)
* From the sample root folder, rename or copy the ./credentials_.js file into ./credentials.js <br />
  * Windows <br />
    ```
    copy credentials_.js credentials.js 
	```
  * OSX/Linux <br />
    ```
    cp credentials_.js credentials.js  
	```
* Replace the placeholders with your own keys in credentials.js, line #23 and #24 <br />
  ```
  client_id: process.env.CONSUMERKEY || '<replace with your consumer key>';
  
  client_secret: process.env.CONSUMERSECRET || '<replace with your consumer secret>';
  ```
* Upload one of your models to your account and get its URN using another workflow sample, for example,
  - [this workflow sample in .Net WPF application](https://github.com/Developer-Autodesk/workflow-wpf-view.and.data.api) if you are using windows 
  - or [this workflow sample in Mac OS Swift](https://github.com/Developer-Autodesk/workflow-macos-swift-view.and.data.api) if you are using Mac
  - or this [WEB page](http://models.autodesk.io/) or this [one](http://javalmvwalkthrough-vq2mmximxb.elasticbeanstalk.com/)
* Copy the URN which was generated in the previous step in file /www/index.js at line #18 <br />
  ```
  var defaultUrn = '<replace with your encoded urn>';
  ```
* Run the server from the Node.js console, by running the following command: <br />
  ```
  node server.js
  ```
* Connect to you local server using a WebGL-compatible browser: [http://localhost:3000/](http://localhost:3000/)


This sample can also work with the Autodesk staging server (vs production) or work with someone else's credentials as long you can get a valid token. 
By default, the project is setup with the production server, and use your own credentials. If you are interested by a different setup, see the Options below.

## Options

You can work with production or staging Autodesk View and Data environments. By default, the project is setup with the production server.

* Instructions to setup this sample to use the Autodesk View & Data staging server are [here](https://github.com/Developer-Autodesk/workflow-node.js-view.and.data.api/blob/master/README-stg.md) 


You can also use someone else credentials to view models using this sample.

* Instructions to setup this sample using someone else credentials are available [here](https://github.com/Developer-Autodesk/workflow-node.js-view.and.data.api/blob/master/README-option.md) 


## License

That samples are licensed under the terms of the [MIT License](http://opensource.org/licenses/MIT). Please see the [LICENSE](LICENSE) file for full details.


## Written by 

Written by [Philippe Leefsma](http://adndevblog.typepad.com/cloud_and_mobile/philippe-leefsma.html)  <br />
(Autodesk Developer Network)

