# Jive Location Demo

## About this Application
The Location Demo app demonstrates many of the core concepts available for most Jive applications. The app retrieves the list of the user's connections from the Jive platform, then retrieves details about each connection's location (time/weather). 
The Location app provides examples of retrieving content from the platform (user's connections), retrieving content from an external RESTful API (location details), posting an update to the activity stream or update the user's status, and instantiating the app using App Mention. 

Key features of the Jive framework implemented by this app are outlined below. 

### Retrieving user's connections
* peopleSearchHandler()

### Retreiving content from RESTful API
* locationSearchHandler(location)
* locationSearchCallback(data)

### Posting status update
* osapi.jive.core.updates.create()

### Posting to activity stream
* osapi.activities.create()

### Mini Message
* new gadgets.MiniMessage()

### User Preferences
* app.xml
* new _IG_Prefs()

### Data Pipelining
* osDataContext.getDataSet()
* &lt;osd:HttpRequest key="KEY" href="URL"/&gt;

### App Mention listener
* gadgets.util.registerOnLoadHandler()


## About the API
The API that powers this application combines services from Yahoo Placefinder and Weather Underground. 
Yahoo was selected over Google's API because Yahoo does not place restrictions on how the search results are used.

* http://developer.yahoo.com/geo/placefinder/
* http://www.wunderground.com/weather/api/

The API uses the free service tier from Wunderground, which restricts the number of requests that can be performed per minute/hour/day. 
__Please be kind and avoid using the API outside the appliction__. 


## Third-Party Libraries
A few additional libraries, beyond jQuery, were used in this app. 

### MomentJS
A lightweight library for parsing and manipulating date objects. Useful in this app when applying timezone offsets for each location. 
http://momentjs.com/

### Mustache
A logic-less templating engine that combines JSON with a template to produce anything you like. Can be use on both the client and on the server. 
http://mustache.github.com/

If you like Mustache, but want the benefit of logic (if/then, for loops, etc) in your templates, check out HandlebarsJS.
http://handlebarsjs.com/


## Learn More
Get Involved in the Jive Developer Community
* https://community.jivesoftware.com/community/developer/
* https://community.jivesoftware.com/community/developer/api

The 'Hello World' Example
* https://developers.jivesoftware.com/community/docs/DOC-1115

Using the Dev Console
* https://developers.jivesoftware.com/community/docs/DOC-1513

Integrating App Mentions (!App) into a Jive app
* https://developers.jivesoftware.com/community/docs/DOC-1628
* https://developers.jivesoftware.com/community/docs/DOC-1744
* https://developers.jivesoftware.com/community/docs/DOC-1743

Data Pipelining
* http://opensocial-resources.googlecode.com/svn/spec/trunk/Core-Gadget.xml#DataPipelining
* http://opensocial-resources.googlecode.com/svn/spec/trunk/Core-Gadget.xml#DataPipelining-ProxiedContent

Accessing data via Jive Connects API
* https://developers.jivesoftware.com/community/docs/DOC-1118
* https://developers.jivesoftware.com/community/docs/DOC-1094
