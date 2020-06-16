<h2>Postman-pinterestExamples</h2>
<h2>Description</h2>
<p align="justified">This repository is to make request to SWAPI API. All the data is accessible through HTTP web API. https://swapi.dev</br>
Below a basic guide on how to install the tests,run, architecture folder structure and useful resources.</p>

<h2>Architecture folder structure</h2>
<ul>
  <li>Environment > Contains the environment file to be used with postman </li>
  <li>reportFormatter > template-default-colored.hbs Contains the report used for command line run</li>
  <li>SWAPI.postman_collection.json Collection of request made in postman</li>
</ul>

<h2>Install</h2>
<p>Postman application is open source software, a Javascript application designed to load test functional behavior. Postman's features simplify each step of building an API and streamline collaboration so you can create better APIs—faster. This repository is using version 7.26.0 The tool can be downloaded at: https://www.postman.com/downloads/</br>\
Postman test can be run from command line using node.js https://nodejs.org/es/
</p>

<h2>Run Tests: </h2>
<h3>How to run tests locally using Postman</h3>
<ul>
  <li>Install Postman</li>
  <li>Double click to open postman</li>
  <li>In the top menu go to File > Import</li>
  <li>Locate in your local machine the file with the postman_collection extension (SWAPI.postman_collection.json)</li>
  <li>Click on the gear in the right top "manage environments" and choose from your local machine the file with the environent extension</li>
  <li>Click on "Import" button</li>
  <li>There are two ways to send request: The first one is click on each request and then click button "send". The other one is to click button in the top menu "Runner"</li>
  <li>The first one is click on each request and then click button "send". The other one is to click button in the top menu "Runner"</li>
  <li>The other one is to click button in the top menu "Runner", select the collection to run and the environment to be used and click button "Start Run". Within this option the number of iterations can be set up manually so the runner will be exceuted "n" times. This option also allows to add delays between each request.</li>
 </ul>
<h3>How to run tests from the command line</h3>
<ul>
  <li>To run the testplan from the command line you need to open a command prompt of Node.js</li>
  <li>Traverse locally until folder where postman test are located</li>
  <li>Run the command: newman run with the following parameters: </il>
    <li>Parameters:
<ol>- Path to the collection name</ol>
<ol>-folder name to run (if applies)</ol>
<ol>-environment to use</ol>
<ol>-the last path is the one where you will store the report formatter (the formatter is located in this repo for your convenience)
finally the last part has the name of the html file where you will find the results of the test.</ol>
</li>
<li>Example:  newman run C:\git\Projects\Pinterest collection of tests.json -e C:\git\Projects\environments\PinterestEnvironment.json --delay-request 2000 --reporters cli,html --reporter-html-export PostmanResult.html</li>
<li>Note: the postman files must have the extension .json in order to be used with newman, otherwise will not be recognized</li>
</ul>
    
<h2>External references: </h2>
<ul>
<li><a href="https://learning.postman.com/docs/postman/collection-runs/command-line-integration-with-newman/">Command line integration with newman</a></li>  
<li><a href="https://swapi.dev/">SWAPI API documentation</a></li>  

