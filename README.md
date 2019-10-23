# BeWhere Connector
- A simple connector to the BeWhere Service

## Pre-requisites
- account in BeWhere Service
- underscore module installed in Scriptr.io IDE


## Configure the connector

- edit the file ./config
```javascript
//The bewhere Info 
const bewhere = {
    baseUrl: "api.bewhere.com",
    endPoint: "https://api.bewhere.com/",
    name: "BeWhere ACOUNT NAME",//not used for now but it will help you distinguish your apps
   
  	username: "<USER_NMAE>",
  	apiKey:"<api_token>",
    accountId:"<account_id>",
};

```
## Use the connector
```javascript
var bwModule = require('./BeWhere');

var bw=new bwModule.BeWhere();
var cnMngr=bw.getConnectorManager();
var myConnector=cnMngr.getConnector();


try{
    
    var result= myConnector.getTypesBeacons();
  	return result;
}catch(exception){
    return exception;
}
```
