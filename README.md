# SPS-7370-Smart-Restaurant-Bot
Smart Restaurant Bot
https://web-chat.global.assistant.watson.cloud.ibm.com/preview.html?region=eu-gb&integrationID=f875a936-91c6-420d-8111-35c986581f0d&serviceInstanceID=2b7174ab-f20b-4f7b-ad9a-a03810ba74b0



Name- Mrs.Disha Sushant Wankhede
Institution Mail Id- disha.wankhede@viit.ac.in




1 INTRODUCTION


Now day’s automation systems are everywhere whether its home, office or any big industry, all are equipped with automation systems. Restaurants/Hotels are also adopting recent automation trends and are installing robots to deliver food and tablets for taking orders. Using these digital menu cards like tablets, customers can easily select the items. This information will be sent to the kitchen of the Restaurant and also displayed on the display.

  1.1  Overview

In this project, a chatbot is developed using Watson assistant. This Chatbot provides following capabilities:
•	Generates the menu list available in restaurant.
•	Different offer show which available in restaurant.
•	Different specials menu show
•	After selecting the menu.
•	Payment mode also available i.e UPI, COD, or Card 
•	The bot is in the position to confirm the order.



  1.2  Purpose

The purpose of a Chatbot is to give immediate responses to the users  Frequently Answered Questions (FAQs) and provide services efficiently.


2 LITERATURE SURVEY



  2.1  Existing problem


Artificial intelligence is on its way to a faster human lifestyle in an efficient way. Virtual bots have become handy nowadays by supporting various domains for smooth lives. Chatbots are helping many sectors by providing services in the form of information agents by effectively accomplishing tasks.


  2.2 Proposed solution

Develop an end to end mobile application capable of managing/placing orders, displaying recommendations, showing the menu, prompting the best deals or collecting the customer feedback using the IBM Watson Assistant. The customer and the order details are stored in the Cloudant DB. Alert is sent when the order is confirmed using the Cloud Messaging. Speech to Text and Text to Speech Services must be used to take the speech input and give out the speech output.


Features
Using chatbot we can manage users reservations and orders
We can give food recommendations and  display the menu to the users
We can Promote best deals and offers on that day
We will store the customer’s details and orders in the database
Chat will send a notification to customers if the order is confirmed
The chatbot is also useful in Follow up on customer feedback

3 THEORITICAL ANALYSIS


  3.1  Block diagram

 

Figure 1. Block Diagram


  3.2  Hardware / Software designing

Figure 2. Flow diagram of Node Red Application


4 EXPERIMENTAL INVESTIGATIONS



5  FLOWCHART
 Figure 3. Flowchart

6 RESULT

Screenshot:- Nodered UI

Screenshot:- Chatbot Preview Link Output

  
7 ADVANTAGES & DISADVANTAGES

Advantages: 
1) Easy and quick to do the Restaurant Related Activity.
2) We can give order 
3) We can check special /Offer related to menu.
4) We  can access more information
 
Disadvantages: 
1) Need to have knowledge about online transaction
2) Need to have credit card or similar type of payment entity
3) If website for the same is down then you will not be able to give order.


8  APPLICATIONS

Smart Restaurant Bot 


9 CONCLUSION

As a conclusion, this software of project is successfully functioned as the objectives of the project. This project helps to solve the problem faced by the restaurant entrepreneur in the attempt to organize the restaurant more efficiently skilled. It can also be used to reduce the lateness and the error caused on ordering foods by the customers by waiters. By using this system, the complaints about the services are eliminated


10 FUTURE SCOPE

Further enhancements can also be there through which this restaurant bot becomes more automated. 

11 BIBILOGRAPHY

APPENDIX
  A. Source code

Chat Bot JSON File

{
  "output": {
    "generic": [
      {
        "values": [
          {
            "text": "Thank You ,Your order of  $number of $items is placed ,please  pay  using $payment . Your receipt is sent to your $email ."
          }
        ],
        "response_type": "text",
        "selection_policy": "sequential"
      }
    ]
  }
}

NodeRed Json File_ Original

[{"id":"ad1dc02c.ce618","type":"watson-conversation-v1","z":"33638b7b.8328f4","name":"Resto Bot","workspaceid":"9e85b3f5-01b5-40dc-a7c4-e2191ad97991","multiuser":false,"context":true,"empty-payload":false,"service-endpoint":"https://api.eu-gb.assistant.watson.cloud.ibm.com/instances/2b7174ab-f20b-4f7b-ad9a-a03810ba74b0","timeout":"","optout-learning":false,"x":400,"y":100,"wires":[["1b4772a7.eca23d"]]}]

NodeRed Json File_ Provided 


[{"id":"2d57220.49511de","type":"tab","label":"Flow 2","disabled":false,"info":""},{"id":"9e9156c5.f83938","type":"ui_form","z":"2d57220.49511de","name":"","label":"","group":"93943817.fdd3f8","order":0,"width":0,"height":0,"options":[{"label":"Enter your input","value":"input","type":"text","required":true,"rows":null}],"formValue":{"input":""},"payload":"","submit":"submit","cancel":"cancel","topic":"","x":160,"y":200,"wires":[["9f41299f.5852d8"]]},{"id":"9f41299f.5852d8","type":"function","z":"2d57220.49511de","name":"","func":"msg.payload= msg.payload.input;\nreturn msg;","outputs":1,"noerr":0,"x":340,"y":220,"wires":[["c1d2a201.f63c","abfadeea.ec376"]]},{"id":"c1d2a201.f63c","type":"watson-conversation-v1","z":"2d57220.49511de","name":"","workspaceid":"0a199a54-cbb6-483a-8e1f-eb5d7a191ed7","multiuser":false,"context":true,"empty-payload":false,"service-endpoint":"https://api.eu-gb.assistant.watson.cloud.ibm.com/instances/db4304a8-5975-4965-8343-f8878129d326","timeout":"","optout-learning":false,"x":420,"y":360,"wires":[["7cb78b0b.4d0f84","8dbdbf57.08834"]]},{"id":"8dbdbf57.08834","type":"function","z":"2d57220.49511de","name":"","func":"if(msg.payload.output.generic[0].response_type==\"image\"){\n    msg.url = msg.payload.output.generic[0].source\n    msg.payload = msg.payload.output.generic[0].title\n}\nelse{\n    msg.url=\"https://t3.ftcdn.net/jpg/02/20/14/38/240_F_220143804_fc4xRygvJ8bn8JPQumtHJieDN4ORNyjs.jpg\"\n    msg.payload = msg.payload.output.text[0];\n}\nreturn msg;","outputs":1,"noerr":0,"x":550,"y":280,"wires":[["7cb78b0b.4d0f84","10b0576f.e72fb9","e0480af3.79e1a8","6e409a58.f3a404"]]},{"id":"7cb78b0b.4d0f84","type":"debug","z":"2d57220.49511de","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","x":600,"y":420,"wires":[]},{"id":"10b0576f.e72fb9","type":"ui_template","z":"2d57220.49511de","group":"93943817.fdd3f8","name":"","order":5,"width":"6","height":"5","format":"<img ng-src={{msg.url}} alt=\"Image\">","storeOutMessages":true,"fwdInMessages":true,"resendOnRefresh":true,"templateScope":"local","x":800,"y":200,"wires":[[]]},{"id":"e0480af3.79e1a8","type":"ui_audio","z":"2d57220.49511de","name":"","group":"93943817.fdd3f8","voice":"de-DE","always":"","x":780,"y":340,"wires":[]},{"id":"abfadeea.ec376","type":"ui_text","z":"2d57220.49511de","group":"93943817.fdd3f8","order":2,"width":0,"height":0,"name":"","label":"text","format":"{{msg.payload}}","layout":"row-spread","x":260,"y":520,"wires":[]},{"id":"6e409a58.f3a404","type":"ui_text","z":"2d57220.49511de","group":"93943817.fdd3f8","order":2,"width":0,"height":0,"name":"","label":"text","format":"{{msg.payload}}","layout":"row-spread","x":830,"y":420,"wires":[]},{"id":"93943817.fdd3f8","type":"ui_group","z":"","name":"UI","tab":"937a2928.80b0a8","order":1,"disp":true,"width":"6","collapse":false},{"id":"937a2928.80b0a8","type":"ui_tab","z":"","name":"Chatbot","icon":"dashboard","disabled":false,"hidden":false}]
 






