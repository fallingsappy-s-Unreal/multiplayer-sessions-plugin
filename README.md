Steps to Use the Menu System Plugin 
 
1.	Create or open an Unreal Engine 5 project 
(For new projects, it is recommended that you use the Third Person project template, as it already has a working character which is replicated). 
2.	Configure the project to use the Steam Online Subsystem 
•	Go to Edit -> Plugins -> search for Online Subsystem Steam 
•	Check Enabled 
•	Click Restart Now 

![image](https://user-images.githubusercontent.com/43529721/167247971-1428265b-3c71-42f5-af84-a43463ecc593.png)

•	In the project folder, go to Config 

![image](https://user-images.githubusercontent.com/43529721/167247988-e685f11d-4128-4f89-b2f8-2d557934d257.png)

•	Open DefaultEngine.ini 
Add the following to the bottom of DefaultEngine.ini (copy them directly from Unreal Engine’s Documentation page)  https://docs.unrealengine.com/4.27/en-US/ProgrammingAndScripting/Online/Steam/ 

![image](https://user-images.githubusercontent.com/43529721/167247997-f1c30724-cff4-4483-9730-285aa1c918fe.png)  

•	Save and close. The full file should appear as follows (with your project name where it says “MenuSystem”) 
•	Open DefaultGame.ini and add: 

![image](https://user-images.githubusercontent.com/43529721/167248003-f73051a9-1447-485c-b544-0ad7c2d2c1fe.png) 

•	Compile the Visual Studio Project (CTRL + SHIFT + B) 
3.	Add the Plugin to the Project Folder 
•	Copy the Plugins folder into your project: 

![image](https://user-images.githubusercontent.com/43529721/167248008-24caa2a2-6fc7-4d65-a1a6-bd8053515878.png)  

•	Inside Plugins, you should see MultiplayerSessions 
•	Close Unreal Engine and Visual Studio. Delete your Binaries, Intermediate, and Saved folders. Right-click your .uproject and select Generate Visual Studio project files. 
•	Open your Visual Studio project solution (.sln). You should now see a Plugins folder in the Solution Explorer 

![image](https://user-images.githubusercontent.com/43529721/167248016-2c954948-aff3-4bc3-924d-20c974c3f10b.png)  

•	Open your project in Unreal Engine. It will ask if you would like to rebuild modules. Select Yes.  
•	In the Content Browser, click Settings. Check Show Plugin Content. 
•	You will now have two extra folders in the Content Browser: Multiplayer Sessions Content and Multiplayer Sessions C++ Classes. 

![image](https://user-images.githubusercontent.com/43529721/167248020-7e86b313-a502-48a5-b911-386289e5ebfb.png)  

•	Go to the Multiplayer Sessions Content folder. There is a Widget Blueprint called WBP_Menu. 
4.	Create a Lobby Level 
•	Create a new level, and save it in your project (it doesn’t matter where you save it or what you name it) 

![image](https://user-images.githubusercontent.com/43529721/167248028-f0f07c2d-ed31-41d2-9b6d-a528fa6f7024.png)  

•	Open your starting level. 

![image](https://user-images.githubusercontent.com/43529721/167248032-500da4bc-1b5b-4d91-989e-62092b25a52c.png)  

•	Open the Level Blueprint. Use Create Widget to create a new widget, selecting WBP_Menu as the widget class. Connect this to Begin Play. 

![image](https://user-images.githubusercontent.com/43529721/167248035-d6680ca7-5915-4104-9a3e-1b2612fb4775.png)  

•	Drag off of the Return Value output and search for Menu Setup. Select it. 

![image](https://user-images.githubusercontent.com/43529721/167248040-65f167f1-4929-4eb1-b49b-08030f6ade57.png)  

•	Change the Number of Public Connections to the number of players you want in your game 
•	Change the lobby path to the path to your lobby level (use /Game/ instead of /Content/) and leave out the .umap extension. 

![image](https://user-images.githubusercontent.com/43529721/167248046-4bee66d0-3205-4cd8-bc03-348b92f87ca9.png)   

5.	Play Test the Game 
•	Go to Platforms -> <platform> -> Package Project. 

![image](https://user-images.githubusercontent.com/43529721/167248052-fc3c8af0-f7cb-4840-95fb-2a4208b160d0.png)  

•	Create a new folder or select a folder destination 

![image](https://user-images.githubusercontent.com/43529721/167248056-7b952df9-c1b0-4068-834b-3453e4b3546b.png)  

•	Click Select Folder 
•	Upload to a Google drive (or anywhere else) and download it onto a second machine • 	Run the Steam client in the background. Make sure both computers are set to the same region (Steam -> Settings -> Downloads -> Download Region).  

![image](https://user-images.githubusercontent.com/43529721/167248060-a5520d85-0e01-4d3a-92b0-162ececabe32.png)  

•	On one machine, launch the game and click Host • 	On the other machine, launch the game and click Join   
•	Test Play! 
