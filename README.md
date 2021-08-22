# MongoDB-Application
Banking GUI Application ( Python + MongoDB)

#Python
• Goto www.python.org. and scroll to find download option. 
• Look for the recent version and click on it. 
• In the Download page, scroll and choose the executable installer for windows.Click on it and watch it downloading. 
• Meanwhile, create a folder “python” in C drive 
• After downloading the python Installation wizard will start.
• Choose Customize Installation to install it in a traceable (easy) location. And check the ‘add python to path.’ If it show at the bottom. If not we can manually set the path in the environment variables in the system settings.
• Choose the location as c:\Python\Python36
• Hit on install. 
• After successful installation, click on start menu, look for python and click on the exe file … there you are. REPL screen is seen. 
• Set the environment variable path by copying the location of python folder. Open system in the settings and type ‘environment variable ‘. Edit the path, click on new, paste the path copied into that and click ok. 
• Open a terminal and type ‘python’.  There you are…. REPL python coding can be done.  


#VSCODE 
https://code.visualstudio.com/download 
• Choose the windows X 64 installer option.
• Follow the dialogue boxes and agree the terms and conditions. (don’t change the default location)
• If needed choose the Desktop Icon option. 
• Open the VSCODE. 
• Look for the ‘ extention’ icon on the left vertical options bar. Click on it and type’ python’ and install it. Reload the VSCODE.
• Create a folder ‘python’ in desktop and open that folder inside vscode.
• Create a new file in it and type a python code. Run the code by choosing the option.

#MONGODB Installation and setup:

• Visit mongodb.com. 
• Download Mongodb Community server. ‘MSI’ extension file will be downloaded. 
• In the Install wizard, choose the ‘complete’ and click next. Install mongodb as a service as default, run service as network service user. 
• If it asks to install MONGODB COMPASS which the GUI for the mongodb, choose it and install. If not, no worries we can download it separately and install the compass. 
• In C drive, Create a folder data. Create a folder called ‘db’ in it.
• Open the Mongodb in its location. Open it till you find the Bin folder. Copy the bin folder path and set path the environment variable. Or, open the bin folder. Leaving it open, open the command prompt terminal and type cd and paste the bin folder path.
• Type ‘mongod’. The daemons will run and the terminal be listening to your commands from then.
• Keeping that terminal running, open another cmd terminal and type ‘mongo’. You will get the prompt from where you can give mongodb commands.


#Mongdb Compas installation.( if not installed while in previous setup)

• Go to mongodb.com/download center and download compass. Choose server mode.
• After downloading go to the Docs in the same page and manual page and click on “installation” on the left.
• Choosing the Mongodb Community server, we can see the entire document on how to download and install this.
• Keeping that as reference, follow the below.
• Click on mongoDB Compass . Download it and install.
• Click it open and click on connect. 
• We need to give the connecting string.Click on “fill in connection field individually” 
• Give your local ip address and local host number. There you go.

#PYMONGO – Installation and configuration.
 
1. Open a cmd promt and type : PIP install pymongo
2. Let the installation start and be complete.
3. If installed…… It is done here.
4. Open vscode and start writing python codes to handle mongodb.
5. Never forget to include “import pymongo” in the python program. 

 ------"A simple python code to create a db in mongodb."-----
 
 Import pymongo.
  create a client. Building connection
 Client=pymongo.MongoClient(‘mongodb:// 127.0.0.1:27107/’)
                                                    (‘ protocol://ipaddress:local host name’)
 creating a dbatabse in mongodb from here.
 Mydb=client[‘employee’] # in the client, planning to create a database by the name ‘employee’.
 we need to create a collection(table)
 collectn=mydb.employee_info        # employee_info is the table name
 let us store record into it.
 records must be in dictionary format/json format.
 record={ “Name”: ‘XYZ’,
 	  “ Age”:27,
 	  “Gender”: ‘M’
 	}
 collectn.insert_one(record) # inserting one record. 
 Note the insert syntax.	
 record1={ “Name”: ‘ABC’,
 	  “ Age”:29,
 	  “Gender”: ‘F’
 	}
 collectn.insert_one(record1) # inserting one record. Note the insert syntax	   
6. If it runs without error, goto mongo CLI and show the dbs and check it.
7. You may also check the same in the compass GUI.



#Import mongo json file.
1. We need to check if the IMPORT tool is active in mongo.
2. Visit: www.mongodb.com/try/download/database-tools
3. Download available MongoDB Database tools.
4. Unzip or extract the same into the mongodb…bin
5. Open a terminal and check mongoimport is available.
6. From the web download a json file for a collection. Or copy this into your system and unzip it. ( I may share it)
7. To download a json file into mongodb,Type:
   Mongoipmort –db dbname –collection collection_name – file the Jason file name along with path 
8. To check if it imported correctly.. goto mongo and  show dbs;
   Show collections;
   Db.collectionname.find() display all the records in the table. 
