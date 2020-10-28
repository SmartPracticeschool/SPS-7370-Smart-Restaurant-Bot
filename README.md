# SPS-7370-Smart-Restaurant-Bot
Smart Restaurant Bot
https://web-chat.global.assistant.watson.cloud.ibm.com/preview.html?region=eu-gb&integrationID=f875a936-91c6-420d-8111-35c986581f0d&serviceInstanceID=2b7174ab-f20b-4f7b-ad9a-a03810ba74b0


https://node-red-zfgje.eu-gb.mybluemix.net/red/#flow/3a419665.ddfc3a
https://node-red-zfgje.eu-gb.mybluemix.net/ui

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

Skill-Disha_Bot   JSON File

{
  "intents": [
    {
      "intent": "enquiry",
      "examples": [
        {
          "text": "Can you please provide menu list?"
        },
        {
          "text": "I want to book into the menu"
        },
        {
          "text": "What are the Offers available?"
        },
        {
          "text": "What are the special item today?"
        }
      ],
      "description": ""
    },
    {
      "intent": "order_place",
      "examples": [
        {
          "text": "Can u please take the order"
        },
        {
          "text": "Can you please take my order"
        },
        {
          "text": "I want to place order"
        }
      ],
      "description": ""
    }
  ],
  "entities": [
    {
      "entity": "email",
      "values": [
        {
          "type": "patterns",
          "value": "email",
          "patterns": [
            "[a-z0-9._%+-]+@[a-z0-9.-]+\\.[a-z]{2,}$"
          ]
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "enquiry",
      "values": [
        {
          "type": "synonyms",
          "value": "deal",
          "synonyms": [
            "deals"
          ]
        },
        {
          "type": "synonyms",
          "value": "item",
          "synonyms": [
            "items"
          ]
        },
        {
          "type": "synonyms",
          "value": "menu",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "offers",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "specials",
          "synonyms": [
            "item",
            "items"
          ]
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "items",
      "values": [
        {
          "type": "synonyms",
          "value": "burger",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Non veg Sandwich",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Paneer Masala",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Pizza",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Veg Pasta",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Veg Sandwich",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Zingy Parcel",
          "synonyms": []
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "order_place",
      "values": [
        {
          "type": "synonyms",
          "value": "order",
          "synonyms": [
            "allowing",
            "allows",
            "attempt",
            "attempting",
            "enabling",
            "ordered",
            "orders",
            "permitting",
            "wishing"
          ]
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "payment",
      "values": [
        {
          "type": "synonyms",
          "value": "Card",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "COD",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "UPI",
          "synonyms": []
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "specials",
      "values": [
        {
          "type": "synonyms",
          "value": "Burger",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "non veg sandwich",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Paneer Masala",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Pasta",
          "synonyms": [
            "mozzarella",
            "pastas"
          ]
        },
        {
          "type": "synonyms",
          "value": "Pizza",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "veg pasta",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Veg Sandwich",
          "synonyms": []
        },
        {
          "type": "synonyms",
          "value": "Zingy Parcel",
          "synonyms": []
        }
      ],
      "fuzzy_match": true
    },
    {
      "entity": "sys-number",
      "values": [],
      "fuzzy_match": true
    }
  ],
  "metadata": {
    "api_version": {
      "major_version": "v2",
      "minor_version": "2018-11-08"
    }
  },
  "dialog_nodes": [
    {
      "type": "standard",
      "title": "Anything else",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "I didn't understand. You can try rephrasing."
              },
              {
                "text": "Can you reword your statement? I'm not understanding."
              },
              {
                "text": "I didn't get your meaning."
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "conditions": "anything_else",
      "dialog_node": "Anything else",
      "previous_sibling": "node_7_1603467781495",
      "disambiguation_opt_out": true
    },
    {
      "type": "event_handler",
      "parent": "node_7_1603467781495",
      "event_name": "focus",
      "dialog_node": "handler_1_1603468020792",
      "previous_sibling": "node_10_1603470359417"
    },
    {
      "type": "event_handler",
      "output": {
        "text": {
          "values": [
            "Can you please provide me the item name that you want "
          ],
          "selection_policy": "sequential"
        }
      },
      "parent": "slot_4_1603468022275",
      "event_name": "focus",
      "dialog_node": "handler_3_1603468022288",
      "previous_sibling": "handler_8_1603468022288"
    },
    {
      "type": "event_handler",
      "output": {
        "text": {
          "values": [
            "How many do you want ?"
          ],
          "selection_policy": "sequential"
        }
      },
      "parent": "slot_3_1603468740585",
      "event_name": "focus",
      "dialog_node": "handler_6_1603468740586",
      "previous_sibling": "handler_7_1603468740586"
    },
    {
      "type": "event_handler",
      "output": {},
      "parent": "slot_3_1603468740585",
      "context": {
        "number": "@sys-number"
      },
      "conditions": "@sys-number",
      "event_name": "input",
      "dialog_node": "handler_7_1603468740586"
    },
    {
      "type": "event_handler",
      "output": {},
      "parent": "slot_10_1603468774641",
      "context": {
        "payment": "@payment"
      },
      "conditions": "@payment",
      "event_name": "input",
      "dialog_node": "handler_7_1603468774642"
    },
    {
      "type": "event_handler",
      "output": {},
      "parent": "slot_4_1603468022275",
      "context": {
        "items": "@items"
      },
      "conditions": "@items",
      "event_name": "input",
      "dialog_node": "handler_8_1603468022288"
    },
    {
      "type": "event_handler",
      "output": {
        "text": {
          "values": [
            "We can accept COD,UPI and Card what is your mode of payment?"
          ],
          "selection_policy": "sequential"
        }
      },
      "parent": "slot_10_1603468774641",
      "event_name": "focus",
      "dialog_node": "handler_9_1603468774642",
      "previous_sibling": "handler_7_1603468774642"
    },
    {
      "type": "standard",
      "title": "Delete Context",
      "output": {
        "deleted": "<?context.remove('items')?><?context.remove('number')?><?context.remove('payment')?><?context.remove('email')?",
        "generic": [
          {
            "values": [],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_7_1603467781495",
      "conditions": "true",
      "dialog_node": "node_10_1603470359417"
    },
    {
      "type": "standard",
      "title": "email",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Hello , Thank You for giving your mail id  $email is it for further references. "
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "Welcome",
      "context": {
        "email": "@email.literal"
      },
      "conditions": "@email",
      "dialog_node": "node_10_1603472772990"
    },
    {
      "type": "standard",
      "title": "enquiry",
      "metadata": {
        "_customization": {
          "mcr": true
        }
      },
      "conditions": "#enquiry || @enquiry",
      "digress_in": "returns",
      "dialog_node": "node_2_1603463340455",
      "digress_out": "allow_all_never_return",
      "previous_sibling": "Welcome"
    },
    {
      "type": "frame",
      "title": "order_palce",
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
      },
      "next_step": {
        "behavior": "skip_user_input"
      },
      "conditions": "#order_place && @order_place",
      "digress_in": "does_not_return",
      "dialog_node": "node_7_1603467781495",
      "digress_out": "allow_all",
      "previous_sibling": "node_2_1603463340455",
      "digress_out_slots": "allow_returning"
    },
    {
      "type": "standard",
      "title": "specials",
      "parent": "node_2_1603463340455",
      "metadata": {
        "_customization": {
          "mcr": true
        }
      },
      "conditions": "@specials",
      "dialog_node": "node_9_1603466848292"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Is cost is 150 per plate"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_9_1603466848292",
      "conditions": "@specials:(Burger)",
      "dialog_node": "response_10_1603467151631",
      "previous_sibling": "response_5_1603467123870"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Is cost is 200 per plate"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_9_1603466848292",
      "conditions": "@specials:(Paneer Masala)",
      "dialog_node": "response_1_1603467042239",
      "previous_sibling": "response_6_1603466955069"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Is cost is 150 per plate"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_9_1603466848292",
      "conditions": "@specials:(Veg Sandwich)",
      "dialog_node": "response_4_1603467062378",
      "previous_sibling": "response_1_1603467042239"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Is cost is 50 per plate"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_9_1603466848292",
      "conditions": "@specials:(Zingy Parcel)",
      "dialog_node": "response_5_1603467123870",
      "previous_sibling": "response_7_1603467084899"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Is cost is 100 per plate"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_9_1603466848292",
      "conditions": "@specials:(veg pasta)",
      "dialog_node": "response_6_1603466955069"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "title": "Special Items",
            "options": [
              {
                "label": "Pizza",
                "value": {
                  "input": {
                    "text": "Pizza"
                  }
                }
              },
              {
                "label": "Paneer Masala",
                "value": {
                  "input": {
                    "text": "Paneer Masala"
                  }
                }
              },
              {
                "label": "Veg Pasta",
                "value": {
                  "input": {
                    "text": "Veg Pasta"
                  }
                }
              },
              {
                "label": "Veg Sandwich ",
                "value": {
                  "input": {
                    "text": "Veg Sandwich "
                  }
                }
              },
              {
                "label": "Burger",
                "value": {
                  "input": {
                    "text": "Burger"
                  }
                }
              },
              {
                "label": "Zingy Parcel",
                "value": {
                  "input": {
                    "text": "Zingy Parcel"
                  }
                }
              },
              {
                "label": "Non veg Sandwich",
                "value": {
                  "input": {
                    "text": "Non veg Sandwich"
                  }
                }
              }
            ],
            "response_type": "option"
          }
        ]
      },
      "parent": "node_2_1603463340455",
      "conditions": "@enquiry:specials",
      "dialog_node": "response_7_1603464897321",
      "previous_sibling": "response_8_1603464584961"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Is cost is 300 per plate"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_9_1603466848292",
      "conditions": "@specials:(non veg sandwich)",
      "dialog_node": "response_7_1603467084899",
      "previous_sibling": "response_4_1603467062378"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Is cost is 350 per plate"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_9_1603466848292",
      "conditions": "@specials:(Pizza)",
      "dialog_node": "response_7_1603467194995",
      "previous_sibling": "response_10_1603467151631"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "We are having 20% off on vegetarian "
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          },
          {
            "values": [
              {
                "text": "We have 10% off on all  non veg menu for women day special discount."
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          },
          {
            "values": [
              {
                "text": "We are having 10% discount on fast food."
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "parent": "node_2_1603463340455",
      "conditions": "@enquiry:offers",
      "dialog_node": "response_8_1603464584961",
      "previous_sibling": "response_9_1603463590525"
    },
    {
      "type": "response_condition",
      "output": {
        "generic": [
          {
            "title": "Menu",
            "source": "https://im1.dineout.co.in/images/uploads/restaurant/sharpen/4/j/o/m41327-15239489375ad59d896b40e.jpg",
            "response_type": "image"
          }
        ]
      },
      "parent": "node_2_1603463340455",
      "conditions": "@enquiry:menu",
      "dialog_node": "response_9_1603463590525",
      "previous_sibling": "node_9_1603466848292"
    },
    {
      "type": "slot",
      "parent": "node_7_1603467781495",
      "variable": "$payment",
      "dialog_node": "slot_10_1603468774641",
      "previous_sibling": "slot_3_1603468740585"
    },
    {
      "type": "slot",
      "parent": "node_7_1603467781495",
      "variable": "$number",
      "dialog_node": "slot_3_1603468740585",
      "previous_sibling": "slot_4_1603468022275"
    },
    {
      "type": "slot",
      "parent": "node_7_1603467781495",
      "variable": "$items",
      "dialog_node": "slot_4_1603468022275",
      "previous_sibling": "handler_1_1603468020792"
    },
    {
      "type": "standard",
      "title": "Welcome",
      "output": {
        "generic": [
          {
            "values": [
              {
                "text": "Hello. I am Restaurant Bot ,  How can I help you? Can you please provide your name and  mail id"
              }
            ],
            "response_type": "text",
            "selection_policy": "sequential"
          }
        ]
      },
      "conditions": "welcome",
      "dialog_node": "Welcome"
    }
  ],
  "counterexamples": [],
  "system_settings": {
    "off_topic": {
      "enabled": true
    },
    "disambiguation": {
      "prompt": "Did you mean:",
      "enabled": true,
      "randomize": true,
      "max_suggestions": 5,
      "suggestion_text_policy": "title",
      "none_of_the_above_prompt": "None of the above"
    },
    "system_entities": {
      "enabled": true
    },
    "human_agent_assist": {
      "prompt": "Did you mean:"
    },
    "spelling_auto_correct": true
  },
  "learning_opt_out": false,
  "name": "Disha_Bot",
  "language": "en",
  "description": ""
}



NodeRed Json File_ Original

[{"id":"ad1dc02c.ce618","type":"watson-conversation-v1","z":"33638b7b.8328f4","name":"Resto Bot","workspaceid":"9e85b3f5-01b5-40dc-a7c4-e2191ad97991","multiuser":false,"context":true,"empty-payload":false,"service-endpoint":"https://api.eu-gb.assistant.watson.cloud.ibm.com/instances/2b7174ab-f20b-4f7b-ad9a-a03810ba74b0","timeout":"","optout-learning":false,"x":400,"y":100,"wires":[["1b4772a7.eca23d"]]}]

NodeRed Json File_ Provided 


[{"id":"2d57220.49511de","type":"tab","label":"Flow 2","disabled":false,"info":""},{"id":"9e9156c5.f83938","type":"ui_form","z":"2d57220.49511de","name":"","label":"","group":"93943817.fdd3f8","order":0,"width":0,"height":0,"options":[{"label":"Enter your input","value":"input","type":"text","required":true,"rows":null}],"formValue":{"input":""},"payload":"","submit":"submit","cancel":"cancel","topic":"","x":160,"y":200,"wires":[["9f41299f.5852d8"]]},{"id":"9f41299f.5852d8","type":"function","z":"2d57220.49511de","name":"","func":"msg.payload= msg.payload.input;\nreturn msg;","outputs":1,"noerr":0,"x":340,"y":220,"wires":[["c1d2a201.f63c","abfadeea.ec376"]]},{"id":"c1d2a201.f63c","type":"watson-conversation-v1","z":"2d57220.49511de","name":"","workspaceid":"0a199a54-cbb6-483a-8e1f-eb5d7a191ed7","multiuser":false,"context":true,"empty-payload":false,"service-endpoint":"https://api.eu-gb.assistant.watson.cloud.ibm.com/instances/db4304a8-5975-4965-8343-f8878129d326","timeout":"","optout-learning":false,"x":420,"y":360,"wires":[["7cb78b0b.4d0f84","8dbdbf57.08834"]]},{"id":"8dbdbf57.08834","type":"function","z":"2d57220.49511de","name":"","func":"if(msg.payload.output.generic[0].response_type==\"image\"){\n    msg.url = msg.payload.output.generic[0].source\n    msg.payload = msg.payload.output.generic[0].title\n}\nelse{\n    msg.url=\"https://t3.ftcdn.net/jpg/02/20/14/38/240_F_220143804_fc4xRygvJ8bn8JPQumtHJieDN4ORNyjs.jpg\"\n    msg.payload = msg.payload.output.text[0];\n}\nreturn msg;","outputs":1,"noerr":0,"x":550,"y":280,"wires":[["7cb78b0b.4d0f84","10b0576f.e72fb9","e0480af3.79e1a8","6e409a58.f3a404"]]},{"id":"7cb78b0b.4d0f84","type":"debug","z":"2d57220.49511de","name":"","active":true,"tosidebar":true,"console":false,"tostatus":false,"complete":"false","x":600,"y":420,"wires":[]},{"id":"10b0576f.e72fb9","type":"ui_template","z":"2d57220.49511de","group":"93943817.fdd3f8","name":"","order":5,"width":"6","height":"5","format":"<img ng-src={{msg.url}} alt=\"Image\">","storeOutMessages":true,"fwdInMessages":true,"resendOnRefresh":true,"templateScope":"local","x":800,"y":200,"wires":[[]]},{"id":"e0480af3.79e1a8","type":"ui_audio","z":"2d57220.49511de","name":"","group":"93943817.fdd3f8","voice":"de-DE","always":"","x":780,"y":340,"wires":[]},{"id":"abfadeea.ec376","type":"ui_text","z":"2d57220.49511de","group":"93943817.fdd3f8","order":2,"width":0,"height":0,"name":"","label":"text","format":"{{msg.payload}}","layout":"row-spread","x":260,"y":520,"wires":[]},{"id":"6e409a58.f3a404","type":"ui_text","z":"2d57220.49511de","group":"93943817.fdd3f8","order":2,"width":0,"height":0,"name":"","label":"text","format":"{{msg.payload}}","layout":"row-spread","x":830,"y":420,"wires":[]},{"id":"93943817.fdd3f8","type":"ui_group","z":"","name":"UI","tab":"937a2928.80b0a8","order":1,"disp":true,"width":"6","collapse":false},{"id":"937a2928.80b0a8","type":"ui_tab","z":"","name":"Chatbot","icon":"dashboard","disabled":false,"hidden":false}]
 






