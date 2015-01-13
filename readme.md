# Romulus

Romulus allows you to build applications without a backend. You just get a datastore and lambda functionality. 

User interface provides a repl and javascript writing. 

You can write lambda functions, and they get set up on aws.

Datastore is managed by Parse. 

You can assign user structure and object store with parse's stuff. 


## Middleware

 - New user signups and access to lambda/parse
 - Storing user data 
 - Serving sites, sending data to cloudfront
 - Store subdomains
 - Store lambda functions and associate them with users
 
## Setup

The following vendor files are required:
```
ace.js
jqconsole.min.js
mousetrap.min.js
normalize.css
```