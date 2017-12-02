RTS (Realtime scrapper) is a tool developed to scrap all pasties,github,reddit..etc in real time to identify occurrence of search terms configured. Upon match an email will be triggered. Thus allowing company to react in case of leakage of code, any hacks tweeted..etc.. and harden themselves against an attack before it goes viral.

The same tool in malicious user hands can be used offensively to get update on any latest hacks, code leakage etc..

Before to use this tool is is neccessary to understand the properties file present in scrapper_config directory.  

  consumer.properties: Holds all the neccessary config data needed for consumer (Refer apache Kafka guide for more information).  
  producer.properties: Holds all the neccessary config data needed for Producer (Refer apache Kafka guide for more information).  
  email.properties: Configure SMTP server with email id's.  
  scanner-configuration.properties: This is the core configuration file. Update all the data of twitter for enabling search on twitter. For   pastie/github and reddit there is no need for any changes in config.  
  However in all cases make sure to change "searchterms" to values of our choice to search. If there are multiple search terms then add  
  them seperate by comma as shown with example terms in config file.  

How to use the tool:  

Install JDK     
Start the zookeeper and Kafka Server (Refer https://kafka.apache.org/documentation/#quickstart for more information)    
Create a kafka topic   
Navigate to scraptool/tartget  
Run the command "java -jar scraptool-1.0-SNAPSHOT-standalone.jar -t <Kafka Topic name> -c <complete path of config directory>"     


Some more tweaking and testing is needed before this code is ready for prod.

Contributors :

  Naveen Rudrappa                                                                                                                        
  Padma Shivakumar
