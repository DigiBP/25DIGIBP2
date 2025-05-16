# GWP Training Program: Process Flow from Planning to Certificate Creation


# Introduction 📥




# Team Members 👥
| Name |
| ------------- |
| Moritz Steiger | 
| Sandro Premier | 
| Juan Camilo Ramírez Gutiérrez | 
| Anaïs von Dach | 
| Micaela Palma Costa | 

# Coaches 📌
- Andreas Martin
- Charuta Pande
- Devid Montecchiari

 

 # AS-IS Process 🚩
The current training program process at GWP is structured but involves multiple tools and manual steps across various platforms. As such there are quite a few inefficiciencies and opporunity to eliminate manual tasks, copy-pasting activities, and potential human errors. It starts with internal planning, where training dates are coordinated, and calendar invitations for Microsoft Teams sessions are sent to speakers via Outlook. Simultaneously, a registration page is created in Pimcore, containing a detailed training agenda and an online registration form available in both German and English. Once the form is published, an email invitation with a link to the registration page is created in Inxmail and distributed via a contact list managed in CAS, the CRM system.

When participants register through the form, Pimcore automatically sends personalized confirmation emails for each selected session, including Microsoft Teams access links and calendar entries. All registration submissions are also forwarded as notification emails to a shared inbox. The responsible team manually processes these registrations by creating contact entries in CAS, linking them to each selected training, and organizing emails by marking them as processed and moving them to designated folders in Outlook.

The day before each training, the final registration list is exported from CAS as an Excel file and saved on the shared network drive. An email notification with a link to the list is sent to the speakers. On the day of the training, the session is conducted and recorded via Microsoft Teams. Attendance is tracked during the session by updating the registration list: present participants are marked, additional attendees are added, and no-shows are noted. After the training, a Teams log of logged-in users is saved as an Excel file on the network drive for documentation purposes.

Certificates of participation are typically prepared the following day. A Word template is filled via mail merge using the final attendance list, saved as a PDF, and split into individual files named per participant. These certificates, along with the presentation slides, are then emailed—usually grouped by company—to the attendees.

Participants who miss the live session can complete the training via self-study. The recorded session is edited to anonymize external attendees and remove breaks, then uploaded to the Share platform. These participants receive an email with links to the video and the presentation, along with a self-study test in PDF format. In order to receive a certificate, the test must be completed and passed. Once the completed test is submitted and meets the required standard, a personalized certificate is issued and sent via email.

![GWP Prozessdiagramm](GWP_Process_As-is_250408.png)

## Involved Roles 🔍
- GWP – Coordinating entity (Advisor for financial service providers)
- Participants – course attendees
- Lecturer – the course facilitators

## Identified Challenges in the Current ("As-is") Process 🚧 
- Manual Work & Media Disruptions: Tasks like "Receive registration mail / Inbox mgmt" or "Export / save Registration list" indicate manual handling, which can be error-prone and time-consuming.
- Communication Delays: Multiple handovers between GWP, Lecturers, and Participants may lead to coordination issues, especially when proposing and confirming training dates.
- Lack of Automation: Steps like "Trigger Inxmail" and "Send confirmation and link" could be automated to improve scalability and reduce administrative overhead.
- Data Handling Issues: Exporting and saving registration data manually raises risks related to data consistency and compliance with data protection standards.

 ## Project Goals :checkered_flag:

# To-Be Process

## Process Improvements

- Process "Training scheduling":
  1) Use of tools like Forms to streamline date coordination with lecturers.
  2) Elimination of manual back-and-forth communication via email or chat.
  3) Grouping of related tasks for better efficiency and visibility.
- Process "Participant Registration":
  1) Automated creation of the registration page using Budibase, including chatbot support for FAQs in terms of courses.
  2) Email campaigns managed via Mailchimp, for automated mail handling through sheduling.
  3) Automatic CRM checks: if a participant is not registered, the system adds them to the CRM and links them to the training.
- Process "Training delivery":
  1) Pre-structured and automatically exported registration lists improve preparation and accuracy.
- Process "Certification creation":
  1) Automatic comparison of the MS Teams log data with the registration list to verify attendance.
  2) Automated sending of certificates, reducing manual document handling.
- Process "Non-atendees handling":
  1) Separation of the non-attendee handling into a dedicated, structured process, rather than embedding it within other steps.
  2) Training recording and material automatically sent to non-attendees via  Make.
  3) Test evaluation automated using decision logic (DMN).
  4) Certificates only generated and sent for passed participants, all handled automatically.




# Implementation

## Process "Training scheduling":
In progress.

## Process "Participant Registration":
![TO-BE Process "Training scheduling"](https://github.com/DigiBP/25DIGIBP2/blob/28effd293130ce4fd00c4af5085058144e00ca15/GWP_Process_ToBe_2_Process%20Participant%20Registration.png)

### Check received answers:

Once a registration has been successfully completed, the corresponding entry in the Google Sheet is automatically updated. In the column "Registration Successful", the value "Yes"    is added.The trigger for this process is a defined date that indicates when registrations are open. From this point on, incoming registrations are processed and the data is cross-    checked with the existing Google Sheet. This ensures that only fully and correctly registered participants are taken into account.
 
<img width="1335" alt="image" src="https://github.com/user-attachments/assets/73abdf4a-23ed-4554-92e5-e7b2689ce4d9" />
  
<img width="1412" alt="image" src="https://github.com/user-attachments/assets/62820053-0c8d-4d68-bdfa-a9326b3878f7" />

### Send confirmation link:

As soon as a registration is successfully completed, participants automatically receive a confirmation email. This email serves as a thank you for the successful registration and includes the link to the corresponding Microsoft Teams meeting. The email is sent automatically, ensuring that all registered participants promptly receive the necessary information for their participation.
 
<img width="971" alt="image" src="https://github.com/user-attachments/assets/bbadac4b-0dc9-48b5-b164-fc4f3861cc23" />
  
<img width="644" alt="image" src="https://github.com/user-attachments/assets/0642c5c2-12e7-4594-a306-786990727e28" />

### Check if participant is in database and if not register participant

In the final step, the system checks whether the registered person already exists in the database. If the person is not found, a new Customer ID is generated, and the essential data, such as the name and email address, is added to the database.

<img width="1077" alt="image" src="https://github.com/user-attachments/assets/f14c42b0-e8fe-4dbd-bc0f-00f1364ecfa2" />

<img width="1214" alt="image" src="https://github.com/user-attachments/assets/be690853-76ae-4dba-8534-8f5bde40e6e9" />


  

## Process "Training delivery":
Out of scope - explain why.

## Process "Certification creation":

### Check the attendance list from the teams against the CRM registration list:
<img width="1254" alt="image" src="https://github.com/user-attachments/assets/fb381bc9-ece3-4acd-ad7a-70493bcbb9b4" />

Once the attendance report is manually exported from Microsoft Teams and transferred into a predefined Google Sheet format, this triggers a semi-automated Make scenario. The process compares the attendance entries with the CRM registration list. When a match is found, the CRM sheet is automatically updated by marking the attendee with "Yes" in the attendance column. This step confirms the first condition required for certificate generation. Due to limited user permissions in Microsoft Teams (student role), this step could only be partially automated.

### If attendance is given, send a certificate to the attendee:
<img width="1237" alt="image" src="https://github.com/user-attachments/assets/ff99c80b-100a-41cb-aa35-54391519770e" />

This process is triggered by a custom webhook and initiates the automated generation and delivery of certificates. The Google Sheets module searches for participants whose attendance has already been confirmed with a "Yes" in the CRM registration sheet — a status that was established in the previous step by matching the Microsoft Teams attendance report with the registration list. Once a matching participant is found, the PDF Generator API creates a personalized certificate. The certificate is then automatically sent to the participant via Gmail. This ensures that only those who actually attended the session receive a certificate, making the process accurate and efficient.

### If attendance is not given, send an email to the non-attendee:
<img width="1322" alt="image" src="https://github.com/user-attachments/assets/45a01a8e-01bc-44a7-acb9-95d6d61bdbb6" />

This process is triggered by a custom webhook and handles participants whose attendance could not be confirmed. It searches the CRM registration sheet for entries where the attendance field is empty or not marked with “Yes”. For each non-attendee, an automated email is sent via Gmail. The message informs them that their attendance could not be verified, and kindly asks them to contact the GWP team. 

# Technologies used 
| Technology | Purpose |
| ------------- |------------------------------------
| Camunda 7 | Workflow automation and BPM execution |
| BPMN 2.0 | Visual language for modeling business processes |
| DMN | Decisions modelling with business rules |
| Make | No-code automation for apps and workflows |
| Cursor | 
| xxxx |


# Outlook



