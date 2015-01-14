# Romulus

Romulus is a "framework" that builds apps comprised of a database and client code. There is no "backend code". All functionalty is handled through client javascript, a javscript database library, and Amazon Lambda functions.

To demonstrate it's utility as an application framework, Romulus is hosted on itself. 

Core functionality currently provided by:

 - **Static Hosting**: S3
 - **Database**: Parse (yes, not a datebase, yet)
 - **Backend "action"**: Amazon Lambda

####Todo:
 1. Get amazon lambda function creation working from the frontend
 2. Replace Parse with a real database

