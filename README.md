Synata's SparkGraphAnalysis class
=========================

Tutorial
=========================
The easiest way to get going is to follow our [Tutorial](Tutorial.md)

Useage
=========================
```
sbt "run load <Gmail Access Token>"
```

This will dump your gmail and load metadata into Mongo.
The easiest way to get your Gmail Access Token is with the Gmail API Playground. Go to:
https://developers.google.com/gmail/api/v1/reference/users/messages/list
and under "Try It" click the "Authorize Oauth" button. Open the developer console, and find the request that ends with /me - Look for the header: 

```
"Authorization: Bearer <TOKEN>" 
```

Copy and paste <TOKEN> into the command.

```
sbt "run analyze"
```

This will run the actual graph analysis (assuming you have data in Mongo)




TODO
=========================
1. Add more configuration options
2. Add retries for usage throttling to the Gmail Loader
