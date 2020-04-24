# simple-chat-bot
Fantasy Football Chatbot Expert System
Abstract 

Chat Bots can be defined as software that uses artificial intelligence to chat with people. Chatbots can be used to carry out tasks such as quickly responding to people, giving better service to customers, informing people, being an FAQ and helping them to purchase products.

The industry that I’m selecting to build a chatbot is the online fantasy sports league industry. Specifically I will be working with fantasy football sports league. This is a multimillion dollar industry, with thousands of leagues that are created every year before football season begins. Every league can be customized however they all follow specific guidelines. Joining a football fantasy league last year, I noticed that I had to get the rules of the league from a certain individual. There was no place where I could find the specific league rules that we had in place. I thought it would be a great idea to have some way of helping new players or even older players confirm the rules of their league. This has many different applications as well, it doesn’t just have to apply to football, it can apply to soccer or hockey or basketball fantasy leagues. For the purposes of this project it will be football specific. The chatbot I will be creating will explain the basic rules of playing in a fantasy football league and will be able to answer questions that new users will have. From what positions to select to how scoring works to how knockout stages in the playoffs work, this chatbot will cover the rules on how to play in fantasy football.

In most Expert Systems there are usually 4 components. A knowledge base, inference engine, working storage and UI. In this case however we do not have a working storage to keep questions that are being asked. I have built a simple GUI that you can run in jupyter notebook. It will prompt you for your question. Once you have asked the question it will then give a reply to what it believes you are asking. I have created 6 classes. Basically there are 7 responses the chat bot can give. It is somewhat basic however the chatbot I built is a very general one. If there was a league, I could implement league specific rules into the bot to answer, but decided to go with an overall FAQ. Once the bot give its response, it will then prompt you if you have another question with yes or no. You reply yes you can ask another question, if you reply no, it will stop. 

Intent Classification (Knowledge Base) 

The dataset that the bot was trained on has 88 rows and 2 columns. One column for the intents and the other for the classes. The intents are the questions we are training the chatbot on and the other is the classification of what the questions are. There are 7 classes; ABOUT, POINTS, PPR, DRAFT, POSITIONS PLAYOFFS and TIEBREAKERS. 

 
Machine Learning Model

I used 3 different models to train my chatbot on. Logistic Regression, Random Forest, Gradient Boosting Classifier. Out of the three models, the Logistic Regression model had the highest results. It showed an accuracy of 80%. The others showed an accuracy of 74% and 76%. Since the dataset was small, I could not implement a NN has it would most likely overfit on such a small training dataset. 

Chatbot Instructions

I have created the model which you can see in the Creating Model.ipynb
I have also provided my dataset which is the chatbotdata2.csv 
 I have also provided the saved pickle model as classifier_pipe.dump
The simple user interface I created is called Final GUI.ipynb
You can just run the Final GUI file if you have the pickle file in the same folder. 


Questions you can ask are: 
What is fantasy football? 
Can you explain what is PPR? 
Who makes playoffs? 
Drafting?
How many positions are there?
What if you are tied?

Conclusion

The chatbot is very simple. I did encounter many different problems that I needed to tackle. I noticed that as a default if you ask questions not related to fantasy football it automatically defaults to class 8 and gives the tiebreaker response. I tried to implement an error threshold and to give an automated response for the chatbot to say please ask again, however I came across difficulties implementing it in my code. My dataset is too small. I needed more data for my model to be trained well. The UI was also very simple, I used ‘if’ and ‘elif’ statements in order to give prewritten responses. In the future, I’d like for the user to input information about their league and give specific information in regards to the league and the user. Maybe it can link to their league and give up to date standings and match up details as to who’s winning during the week. Right now the most that yahoo’s fantasy football league does, is give notifications when teams score a touchdown. I’d like for our chatbot to be implemented on their app and be able to give up to date scores and recommendations on who to play in their line up every week. 
*Please keep in mind, its very simple what I did but there are many errors, in no way is this perfect but a decent starting point for anyone looking to build one from scratch. 
