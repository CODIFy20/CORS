# XXE injection. 
# What is XXE injection? 
XXE injection also known as XML external entity injection. IT is a type of back end web security vulnerability that allows an attacker to interfere with an application's processing of XML data. It often allows an attacker to view files on the application server filesystem, and to interact with any back-end or external systems that the application itself can access. IT works on SYN-ACK type of communication between evil sever and genuine server. It is more applicable in IoT and also known  as one of IoT attacks. XXE injection attack can be escalated by compormising server by using SSRF (server side request forgery).  
![XXE_600x315](https://user-images.githubusercontent.com/115407638/204035060-03d35c3f-eff2-48fb-8fd3-e61cc5bf77c0.png) 

# Steps to perform XXE injection. 
1) Client sends requests to the server XXE data. 
2) Server sends SYN-ACK sommand to evil server. 
3) XXE payload is injected and sent to the genuine server that asks for c:/windows/win.ini 
4) XXE vulnerablity of attacker is exploited. 

# Payloads Used 
1) <!--?xml version="1.0" ?-->
<!DOCTYPE replace [<!ENTITY example "Doe"> ]>
 <userInfo>
  <firstName>John</firstName>
  <lastName>&example;</lastName>
 </userInfo>

# Impact 
XXE injection vulnerablity basically works on data in use and transit data. It can cause the loss of sensitive info of an organisation or an individual. 
