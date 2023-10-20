File location of  files:

// parent folder central            https://drive.google.com/drive/folders/1zWMTHRMfAR3fE3bEp0kOR4QSucNiEbcM

// googleSheet   SAM_central_base   https://docs.google.com/spreadsheets/d/1u_XA584h97AqrzQHfkDPDNhfHCiJ0mdsh9LKy9YFB_E/edit#gid=2137001534

// bound script  centralBase        https://script.google.com/u/0/home/projects/1HNFbwjemWgRXv6FhHuOv4I4X1uyRPSSKhuO1v-qvXiEx2Cqkr7IP9N8e/edit

File 'SAM_central_base' is where management of all file peers for all shelters is carried out. 

A script (script addShelters) should create a peer of files for every shelter in a batch process. 
First the script is getting a peer of template files (SAM_base_v1.1 and SAM_attendance_v1.1) and makes a copy of each one of them (it makes two replicas). This way it is creating a new peer of files for each shelter in the list.
The new peer of files gets as a suffix the name of the shelter for which it was created (eg. SAM_base_xenon1). 
Then the script creates a new sheet in file SAM_central_base. The new sheet should be an exact copy of the SAM_base_[suffix]. Therefore it gets with importrange() the data from SAM_base_[suffix].

To be continued - Documentation for other scripts (such as createIndex, updateIndex, actualize Students) not yet completed.

File location of template files: 
parent folder  fileTemplates  https://drive.google.com/drive/folders/1Uijr4MLujvXXqF7jRdTaIiElItnKTF1A?usp=drive_link
googleSheet    SAM_base_v1.1  https://docs.google.com/spreadsheets/d/1SBdpnEiupcSglaTRn7kYdcGaj0DpOoLy2j-bLd35R4E/edit?usp=sharing
bound script   UpdateAttendance  https://script.google.com/u/0/home/projects/1jAorXN2wRQ8zkvdz41lFrMJ4nnjrm2xNVMmfD3jl0UgQSHzh5myhtyTZ/edit
googleSheet    SAM_attendance_v1.1  https://docs.google.com/spreadsheets/d/1zFRgnibnKa38hnH2A6At1C7YiIHlq-tXni_JFhqxPPY/edit#gid=901827895
bound script    attendance_      https://script.google.com/u/0/home/projects/1C0ZLIBsWKCDxTIfr3bTylpyYdEE8WNOOJT6340z15T7Tx-h_RWiBpaJQ/edit

