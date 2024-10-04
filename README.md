 Log Temperature Sensor Data to Google Sheet using NodeMCU ESP8266
![image](https://github.com/user-attachments/assets/0807f584-f1e0-40d7-8b09-eb7d5f524fb9)



Components Required
1. NodeMCU ESP8266 Module
2. DHT11 Sensor
3. Jumpers

Circuit Diagram
![image1](https://github.com/user-attachments/assets/5cfb82dc-e06a-4328-9e26-2700755093e0)

There will be a few steps before starting to program ESP8266 for Logging Temperature Data on Google Sheet. 
We will be needing few credentials that will be used to communicate and send the data from ESP8266 to Google Server to reflect on Google Sheet.

Creating Google Script in Google Sheet for Data Logging
1. Login to the Gmail with your Email ID and Password.
2. Go to the App Icon In Top Right Corner Highlighted in Green Circle and Click on Docs.
3. The Google Docs screen will appear. Now choose Sheets in the right sidebar.
4. Create a New Blank Sheet.
5. The Blank Sheet will be created with an “Untitled Spreadsheet”. Just rename this created Spreadsheet Project to any name you want.
  In my case I have renamed “Untitled Spreadsheet” to “ESP8266_Temp_Logger” since I am logging temperature using ESP8266.
  To rename the created Spreadsheet Project, go to “File” > “Rename”.
6. You can also add another multiple sheets in Google spread sheet. In this tutorial only one sheet is used.
  So I have renamed “Sheet1” > “TempSheet” since I am logging Temperature data to sheet.
7. After renaming the created Spreadsheet Project and Sheet name, now its time to create a Google script. 
8. Now got to ‘Tools’ marked in green circle and click on “<> Script Editor” option marked on red circle.
9. The new Google Script is created with “Untitled project”. You can rename this Google Script File to any name you want.
  In my Case I have renamed to “Untitled project” > “TempLog_Script”.
10. Now Copy and Paste the Google Script code from file attached in this ZIP file here (GoogleScript.gs).
  Then edit the Sheet name and Sheet ID in the code. You can get the Sheet ID from the Sheet URL just like shown below.
  https://docs.google.com/spreadsheets/d/xxxxxxxxyyyyyyzzzzzzzzzz/edit#gid=0 , where “xxxxxxxxyyyyyyzzzzzzzzzz” is your Sheet I
11. When you copy and paste the Google Script then it will look like following.
12. Save the file. If you want to make your own sheet then change your credentials such as Sheet ID, Sheet Name and Sheet Project Name.
13. Now we have finished the Setting up Google Script in Spreadsheet. Now it’s time to get the major credential i.e. Google Script ID which will be written in the Arduino Program.
  If you make mistake in the copying Google Script ID then the data won’t reach to Google Sheet.

Getting the Google Script ID
1. Go to ‘Publish’ > ‘Deploy as Web App…’
2. The “Project version” will be “New”. Select “your email id” in the “Execute the app as” field. Choose “Anyone, even anonymous” in the “Who has access to the app” field. And then Click on “Deploy”.  
3. You will have to give the Google permission to deploy it as web app. Just click on “Review Permissions”.
4. Then choose your Email ID here using which you have created spreadsheet.
5. Click on “Advanced”.
6. And then click on “Go to ‘your_script_name’(unsafe)”. Here in my case it is “TempLog_Script”.
7. Click on “Allow” and this will give the permission to deploy it as web app.
8. Now you can see the new screen with a given link and named as “Current web app URL”. This URL contains Google Script ID. Just copy the URL and save it somewhere.
9. Now when you copy the code, the format is like <https://script.google.com/macros/s/____Your_Google _ScriptID___/exec>. 


This finishes the complete tutorial on sending the sensor data to a Google sheet using ESP8266.





