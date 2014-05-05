NODE-ChatServerAndClient
========================

Introduction:

This is a basic chat server implemented using Node.js and MySql on server side. 
The chat client has also been implemented using Node.js. Any other technology like iOS, etc can also be used to make a similar client maybe for other devices.

Installation:

1) First install Node.js.
Link: http://nodejs.org/download/
And then install MySQL Workbench.
After installation run ChatServerDB.sql file in MYSQl.
After run script chatserver database is created.

2) Now open node.js command prompt and install socket.io using following command...
npm install socket.io 

3) Next in then node.js command prompt install mysql package using following command...
npm install mysql 

4) Now you must change the path on ChatServer.js
   Open ChatServer.js and edit socket.io physical path and mysql physical path as follows
   Currentlly for socekt.io path is set : socketio = require('c://Users/dev4/node_modules/socket.io/index.js');
   and for mysql the path is set : var mysql = require('c://Users/dev4/node_modules/mysql');

   You have to change this path to wherever you have installed them.

5) Now open Chat.htm file and change the domain path :
   Currentlly it is set "http://192.168.0.32:2525/socket.io/socket.io.js"
   you have to change only "http://192.168.0.32" according to your server.

6) Now Open Main.js and change same domain path :
   Currentlly it is set :   iosocket = io.connect("http://192.168.0.32:2525/");
  You have to change "http://192.168.0.32" according to your server.

7) Now open command prompt and go to the physical location of node_modules folder where your node.js is installed...
   like "D:\workspace\ChatServer\ServerNew>"
   and run node server using following command...    
   node chatserver.js
   like "D:\workspace\ChatServer\ServerNew>node chatserver.js"

8) To use the chat client simply open http://192.168.0.32/chat.htm file in your browser (replacing the server url). Other users accessing your server can do the same and all can chat.


