# google_cloud_functions
 
Utility to save incoming msgs via webhook in Firestore DB and then periodically writing it in Google spreadsheet. 
There are 2 Google cloud functions (serverless functions) written in Node.js. 

Function #1
webhook-firestore => To read payload from incoming POST calls and then saving it in Firestore DB.

Function #2
firestore-spreadsheet => To sync msgs from Firestore DB to Google spreadsheet on periodic basis in order to adhere to number of writes per minute to Google spreadsheet policy. 

Google cloud scheduler => For scheduling writes to Spreadsheet.
