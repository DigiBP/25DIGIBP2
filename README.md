# GWP Training Program: Process Flow from Planning to Certificate Issuance


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

- Process "Training sheduling":
  1) Use of tools like Forms to streamline date coordination with lecturers.
  2) Elimination of manual back-and-forth communication via email or chat.
  3) Grouping of related tasks for better efficiency and visibility.
- Process "Participant Registration":
  1) Automated creation of the registration page using Budibase, including chatbot support for FAQs in terms of courses.
  2) Email campaigns managed via Mailchimp, replacing manual handling in Inxmail.
  3) Automatic CRM checks: if a participant is not registered, the system adds them to the CRM and links them to the training.
- Process "Training delivery":
  1) Pre-structured and automatically exported registration lists improve preparation and accuracy.
  2) ?
- Process "Certification creation":
  1) Automated sending of certificates, reducing manual document handling.
- Process "Non-atendees handling":
  1) Training recording and material automatically sent to non-attendees via  Make.
  2) Test evaluation automated using decision logic (DMN).
  3) Certificates only generated and sent for passed participants, all handled automatically.




# Implementation

# Outlook



