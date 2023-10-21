===================================================================================
=== This manual is no more accurate. Needs to be completly updated and expanded ===
===================================================================================

Deployment

-- Check the fileID for both files "attendance_" and "base_attendance_". 
-- In file "base_attendance" go to tab "ProgramDATA". 
-- Locate the fileID from URL as is displayed in the browser's address bar. The fileID is the part of the URL that uniquely identifies the file. 
Example: in the URL: 
https://docs.google.com/document/d/1p5QwSIzMK7eAoyBslXrrK67Hrzruo0v2M3iNU7XxtY8/edit
the fileID is 1p5QwSIzMK7eAoyBslXrrK67Hrzruo0v2M3iNU7XxtY8
-- The fileIDs of both files are stored in file  "base_attendance_" >>> sheet "ProgramDATA" as variable values. The script at runtime reads from that sheet all variable values needed. In the left column of the table named "VARIABLE_NAMES" are stored the names of the variables and in the middle column named "VARIABLE_VALUES" are stored the corresponding values. The fileID of file "base_attendance_" is stored in section "updateAttendance()" with the name "sourceSS_ID" (in the middle cell of the table). 
-- If the fileID stored there does not match the actual fileID of file "base_attendance_" as it  is displayed in the URL, then copy the actual fileID from URL and paste it into the middle cell corresponding to "sourceSS_ID". In the adjacent cell to the right you will see that this fileID (or the google address) belongs to the file "base_attendance_".
-- Do the same check for the file "attendance_", if needed paste the fileID of file "attendance_" into the corresponding cell ("sourceSS_ID") in section "preserveAttendance()". In the adjacent cell to the right you will see that this fileID (or the google address) belongs to the file "attendance_".
-- Open the file "deployAttendance". Paste the index of shelters after row 2 under the corresponding headers. If the data in the columns do not match the headers, then the variables in the script or/and in the sheet "ProgramDATA" must be adjusted accordingly.
-- Run the script "createReplicaFiles". Open the menu Extensions>>>AppsScript, select the function "createReplicaFiles" and run it. In the log window you will see the output about creating every replica file. To adjust the naming of the replicas, the source or destination locations or other parameters, modify the script accordingly and save it before running.
-- If you wish to run again the script in order to create another folder of replica-file-peers, you should first delete the file links and the URLs from index. The script is first checking for data in these columns of the index and creates replicas just for the shelters having empty cells in the columns for file links / URLs.    
-- The individual replica-peers-of-files are stored in the destination folder, one peer for every shelter: one file "attendance_some_shelter" and one file "base_attendance_some_shelter". Now the file peers can be distributed to the corresponding shelters.

The next steps concerning the initialization of the file-peers should be performed by each shelter. Alternatively they can be performed centrally before sending the links to the replica-file-peers. This way every shelter gets a ready-to-use-file-peer and the initializing overhead falls on the central authority.  

-- The shelter on the very first opening of any of both individual files must allow access to the other file of the peer. Go to cell A1, wait for the message to appear and click on button "Allow". After finishing this procedure for both files, the communication between them is settled forever.
-- Run once updateAttendance() in order to authorize that script to make changes on those files. 
-- In file "base_attendance" go to tab "students". Click the button "Update Attendance".
-- Follow the procedure of authorization .
-- Alternative: run the function updateAttendance() directly from the script editor.
-- If you already have modified some data before running the function updateAttendance() for the very first time, then, after the authorization procedure has finished, run again updateAttendance() in order to execute and to make this time the proper synchronization between the files. The authorization process needs to run just once, just for the very first time. 


