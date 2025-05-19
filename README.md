# GWP Training Program: Process Flow from Planning to Certificate Creation


# Introduction 📥
GWP is a Swiss-based consultancy specializing in governance, risk, and compliance (GRC), with a strong focus on financial services and regulatory requirements. With a team of seasoned professionals, GWP supports banks, insurers, and other institutions in navigating the complex landscape of financial regulation, internal control systems, and risk management. The firm is known for its pragmatic approach, combining deep regulatory expertise with operational implementation support to help clients achieve sustainable compliance and operational excellence.

GWP offers specialized training programs designed to equip customers with practical knowledge in key regulatory and compliance domains. Delivered by experienced practitioners, the courses are tailored to the needs of financial institutions and are available both in-house and as open seminars. The training offer is designed to complement GWP’s consulting services by building internal capabilities and fostering a culture of compliance within client organizations.

Until now, GWP’s training efforts have centered primarily on content delivery and business development, successfully expanding their offering and client base. As the training business has grown, it has become increasingly evident that opportunities for efficiency gains through digitalization exist. In particular, the planning-to-certificate-creation process has emerged as a key area for optimization. This initiative therefore focuses on digitizing and streamlining the end-to-end training process—from initial scheduling to the final delivery of training certificates to participants—in order to enhance operational scalability and improve the overall participant experience.

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
The current training process at GWP is structured but involves multiple tools, isolated data repositories, and manual interventions. It suffers from inefficiencies related to repetitive tasks, copy-pasting between platforms, and the risk of human error due to limited automation.

## 1. Training Planning and Coordination

The process begins with internal planning to determine training dates. Invitations for Microsoft Teams sessions are manually sent via Outlook. This coordination often involves several rounds of back-and-forth, as not all proposed dates suit both GWP coordinators and instructors.

## 2. Registration Page and Promotion (Runs in Parallel with Step 1)

While training dates are still being coordinated, the marketing team begins preparing the registration page in Pimcore. This includes adding the detailed agenda and building the online registration form (available in both German and English).

However, because final training dates are often not confirmed promptly (as noted in Step 1), the publication of the registration page is frequently delayed. Once dates are finalized, a promotional email is created in Inxmail with a link to the registration page. The email is then sent to relevant contacts managed in CAS, GWP’s CRM system.

## 3. Participant Registration and Confirmation

Participants register via the form, triggering Pimcore to send personalized confirmation emails with Teams links and calendar entries. Each registration also sends a notification to a shared inbox. The team manually:

- Creates contact entries in CAS,
- Links them to specific trainings, and
- Sorts emails in Outlook to mark them as processed.

## 4. Pre-Training Preparation

The day before the training, the final participant list is exported from CAS to Excel and saved on the shared network drive. A link to the list is emailed to the instructor.

## 5. Training Delivery and Attendance Tracking

On the day of training, the session is held and recorded via Microsoft Teams. Attendance is tracked in the Excel file:

- Present participants are marked,
- Extra attendees are added,
- No-shows are noted.

A Teams login report is also saved on the shared drive for documentation.

## 6. Certificate Creation and Follow-Up

The following day, certificates are generated using a Word mail merge from the final attendance list. Each certificate is saved as a PDF, split per participant, and emailed—typically grouped by company—along with presentation slides.

## 7. Self-Study for no-shows

Participants who missed the live session can complete the training asynchronously. The Teams recording is edited (to anonymize attendees and remove breaks), then uploaded to Share. These participants receive:

- A link to the video and slides,
- A self-study test (PDF).

Upon passing the test, a personalized certificate is issued and sent via email.

## 📌 BPMN Diagram – AS-IS Training Process at GWP
![GWP Prozessdiagramm](GWP_Process_As-is_250408.png)
> The above BPMN diagram visualizes the current end-to-end training process, highlighting key manual touchpoints and tool handoffs across planning, registration, delivery, and certification stages.

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
  1) After successful registration, the system updates the Google Sheet and ensures only valid entries are considered during the registration period.
  2) Registered participants automatically receive a confirmation email with the Teams link.
  3) Automatic CRM checks: if a participant is not registered, the system adds them to the CRM.
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

<img width="975" alt="Bildschirmfoto 2025-05-18 um 12 27 36" src="https://github.com/user-attachments/assets/d65b3f20-d0be-4b4e-95bd-e772b466aca2" />

### Start-Event
The trainer scheduling process can be initiated either manually or at a predetermined interval (e.g. every 3 months). Starting the process based on a time-triggered event could be useful for continuously checking the availability of trainers and offering respective trainings.

### Update Calendly Event Types
The first step for the coordinator at GWP is to update the Calendly Event Types. Calendly is an external tool that facilitates scheduling meetings between groups. In this case, we use Calendly to allow trainers to provide their availability. Each training offered has its own separate Event Type:

<img width="1060" alt="Bildschirmfoto 2025-05-18 um 12 45 31" src="https://github.com/user-attachments/assets/840824dd-1efe-4981-83d1-692bc15880bc" />

Before sending out the Calendly links, the GWP coordinator must ensure that the Event Types are up to date and include all relevant information. Additionally, the coordinator can block specific time slots when the training facility is unavailable or when a training session should not be scheduled on a particular date or time.
Since this task is implemented as a user task, the GWP coordinator will be prompted to confirm that all Calendly Event Types have indeed been updated:

<img width="761" alt="Bildschirmfoto 2025-05-18 um 12 54 15" src="https://github.com/user-attachments/assets/05b356aa-837b-4663-8679-0f8c4acffa0f" />

### Choose training topic
The next user task is selecting the training topic. In this scenario, GWP offers three different types of training to its customers. The GWP coordinator can choose one of these three topics, and that choice will be used in the next step to match the selection with the corresponding Calendly event types. So the Coordinator picks the training that should be performed next:

<img width="885" alt="Bildschirmfoto 2025-05-18 um 13 17 52" src="https://github.com/user-attachments/assets/fefe7414-2c94-4a32-8249-8bb08ed01125" />

In a more sophisticated setup with a larger pool of lecturers covering diverse fields, this selection could also be leveraged to target those with specific expertise.

### Send link to lecturers




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

<img width="950" alt="image" src="https://github.com/user-attachments/assets/09a86e8a-5623-429b-b1c9-60f9169ab139" />

<img width="852" alt="image" src="https://github.com/user-attachments/assets/8e50535e-f342-4fee-a91a-34d095b89916" />

### Check the attendance list from the teams against the CRM registration list:

<img width="1254" alt="image" src="https://github.com/user-attachments/assets/fb381bc9-ece3-4acd-ad7a-70493bcbb9b4" />

Once the attendance report is manually exported from Microsoft Teams and transferred into a predefined Google Sheet format, this triggers a semi-automated Make scenario. The process compares the attendance entries with the CRM registration list. When a match is found, the CRM sheet is automatically updated by marking the attendee with "Yes" in the attendance column. This step confirms the first condition required for certificate generation. Due to limited user permissions in Microsoft Teams (student role), this step could only be partially automated.

<img width="1170" alt="image" src="https://github.com/user-attachments/assets/d8186c8a-7ad1-4d0f-955e-aebece7dccb0" />


### If attendance is given, send a certificate to the attendee:
<img width="1237" alt="image" src="https://github.com/user-attachments/assets/ff99c80b-100a-41cb-aa35-54391519770e" />

This process is triggered by a custom webhook and initiates the automated generation and delivery of certificates. The Google Sheets module searches for participants whose attendance has already been confirmed with a "Yes" in the CRM registration sheet — a status that was established in the previous step by matching the Microsoft Teams attendance report with the registration list. Once a matching participant is found, the PDF Generator API creates a personalized certificate. The certificate is then automatically sent to the participant via Gmail. This ensures that only those who actually attended the session receive a certificate, making the process accurate and efficient.

<img width="1344" alt="image" src="https://github.com/user-attachments/assets/48f7388e-5879-424d-a3f0-d39af12aa808" />


### If attendance is not given, send an email to the non-attendee:
<img width="1322" alt="image" src="https://github.com/user-attachments/assets/45a01a8e-01bc-44a7-acb9-95d6d61bdbb6" />

This process is triggered by a custom webhook and handles participants whose attendance could not be confirmed. It searches the CRM registration sheet for entries where the attendance field is empty or not marked with “Yes”. For each non-attendee, an automated email is sent via Gmail. The message informs them that their attendance could not be verified, and kindly asks them to contact the GWP team. 

<img width="1177" alt="image" src="https://github.com/user-attachments/assets/cf46da90-deac-48fc-a2d2-c274549cfcbb" />

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



