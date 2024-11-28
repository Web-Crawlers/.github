## Cloud Computing Assignment 1 - Build Something
### Description of the application
We have built a web crawling system split into two microservices and a database.
The first microservice “web-crawl” is written in Python and when given an URL, extract important text content from the web page. The content selection is done using predefined html tags, these can be customised to suit the website one intends to crawl.  This content is then saved in the database. 
The second microservice is a front-end webpage which fetches the previously stored data from the database and displays it. It is mainly written in C#. 
The database is a MongoDB which is set up using Kubernetes via the mongo-compose.yaml file. It is set up using PersistentVolume and Statefulset. It also has a database service which is accessed by the microservices to add to and retrieve from the database respectively. 
