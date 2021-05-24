# Frontline-health-workers-management-app-by-integrating-hospital-database

This code contains the basic design of our idea ,where patient details will be given as input and would be stored in csv file. A unique barcode will be generated for each patient, by scanning which the patient data will be displayed. We also have provision for updating the patient’s data periodically. The other part of the code is to send the notification to the nurses periodically.


# Hardware

• Arduino Uno

• Mini barcode scan engine

• Display

• TP4056 1A Li-Ion Battery Charging Board Micro USB with Current Protection

• Lithium ion battery chargable


# Software
• Python 3

• Arduino 2.0

• DB Browser for SQLITE3


# Process flow
• The patient data is entered into the main database and gets stored in it as csv file

• Unique barcode is generated which also gets stored in csv file, which can be printed.

• The patient data , medications can be updated .

• Notification for each patient will be triggered by the database .

• Other timely notification for the nurses will also be received.

• As the code was getting comlex and the time given to us was not sufficient, the full system code is yet to be done,and also cloud integration is pending.


# Data flow digram
 ![image](https://user-images.githubusercontent.com/84720604/119373748-60eb7900-bcd6-11eb-9010-266298061c9b.png)
 

# Working Structure:

1.Appointment

 • Using DB Browser for SQLITE3, create a database containing the columns ID, Name, Age, Gender, Location, Phone, Appointment_Date
 
 • We add the database file to the python IDE.
 
 • Create frames where we enter the details of the patient and we add appointment which is automatically stored in the database created earlier.
 
2.Update

 • This is where we update the details of the patients when any changes are to be made. It is a simple module where we enter the name of the patient and the required changes can    be made.These updated detail is stored automatically to the database.
 
 • We import the database file to csv and the barcode is generated using the Barcode Format.
 
3.GENERATING NOTIFICATIONS

 • Using pandas, we are reading the csv file and importing datetime library.
 
 • We are arranging the dataset in ascending order with respect to time, to make it convenient to generate notifications in an orderly manner.
 
 • We have grouped the dataset based on the time of dosage, in order to not miss any patients. Just in case, two patients are to be given dosage at the same time notification would be sent at the same time to the nurse.
 
 • From win10toast library, we have imported ToastNotifier module to generate notifications.
 
 • We are reading through each time instance in the dataset and comparing it with the present time, if it matches it generates a notification.
 
 • Nurses’ health is important as well, so we designed a notification system to remind them of their meal breaks and a gratitude message at the end of their shift.
 
 
# Contributed By
SWETHA S

TANUJA D

SUBHIKSHA M

SAI LIKHITHA P
