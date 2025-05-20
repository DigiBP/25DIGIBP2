## Table of Contents

- [Introduction 📥](#introduction-)
- [Team Members 👥](#team-members-)
- [Coaches 📌](#coaches-)
- [AS-IS Process 🚩](#as-is-process-)
  - [1. Training Planning and Coordination](#1-training-planning-and-coordination)
  - [2. Registration Page and Promotion](#2-registration-page-and-promotion-runs-in-parallel-with-step-1)
  - [3. Participant Registration and Confirmation](#3-participant-registration-and-confirmation)
  - [4. Pre-Training Preparation](#4-pre-training-preparation)
  - [5. Training Delivery and Attendance Tracking](#5-training-delivery-and-attendance-tracking)
  - [6. Training Completion Processing](#6-training-completion-processing)
  - [7. Self-Study for no-shows](#7-self-study-for-no-shows)
  - [BPMN Diagram – AS-IS Training Process at GWP](#-bpmn-diagram--as-is-training-process-at-gwp)
- [Project Goals 🏁](#project-goals-checkered_flag)
  - [Involved Roles 🔍](#involved-roles-)
  - [Identified Challenges 🚧](#identified-challenges-in-the-current-as-is-process-)
- [TO-BE Process](#to-be-process)
  - [Process Improvements](#process-improvements)
  - [Implementation](#implementation)
    - [1. Process "Training scheduling"](#process-training-scheduling)
    - [2. Process "Participant Registration"](#process-participant-registration)
    - [3. Process "Training Completion Processing"](#process-training-completion-processing)
- [Technologies used](#technologies-used)


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

## 6. Training Completion Processing 

The following day, certificates are generated using a Word mail merge from the final attendance list. Each certificate is saved as a PDF, split per participant, and emailed—typically grouped by company—along with presentation slides.

## 7. Self-Study for no-shows

Participants who missed the live session can complete the training asynchronously. The Teams recording is edited (to anonymize attendees and remove breaks), then uploaded to Share. These participants receive:

- A link to the video and slides,
- A self-study test (PDF).

Upon passing the test, a personalized certificate is issued and sent via email.
This process step will not be further elaborated in the project work due to time and scope constraints.


## 📌 BPMN Diagram – AS-IS Training Process at GWP
![GWP Prozessdiagramm](GWP_Process_As-is_250408.png)
> The above BPMN diagram visualizes the current end-to-end training process, highlighting key manual touchpoints and tool handoffs across planning, registration, delivery, and certification stages.

# Project Goals :checkered_flag:

The primary goal of this project is to improve the efficiency, scalability, and transparency of GWP’s training program by digitizing and partially automating the end-to-end process—from planning to certificate issuance. Based on the challenges identified in the current (as-is) process, the project focuses on the following objectives:
 
- Enhance Operational Efficiency
- Increase Process Automation
- Improve Data Consistency and Compliance
- Strengthen Participant Experience
- Increase Transparency and Monitoring
 
## Involved Roles 🔍
- GWP – Coordinating entity (Advisor for financial service providers)
- Participants – course attendees
- Lecturer – the course facilitators

## Identified Challenges in the AS-IS Process 🚧 
The current training process at GWP, while structured, presents several challenges that limit efficiency, scalability, and consistency. The following issues have been identified:

- **Manual Work & Media Disruptions**  
  Many process steps rely on manual handling and switching between tools. Tasks such as managing incoming registration emails or exporting and saving participant lists are time-consuming and error-prone. These media disruptions increase the likelihood of mistakes and slow down execution.

- **Communication Delays**  
  Coordination between GWP, lecturers, and participants—particularly around setting and confirming training dates—often involves several rounds of back-and-forth communication. This leads to delays in publishing registration materials and complicates scheduling.

- **Lack of Automation**  
  Several actions that could be automated—such as sending confirmation emails or launching promotional campaigns—still require manual intervention. This not only increases the administrative workload but also reduces responsiveness and scalability as training volumes grow.

- **Data Handling Issues**  
  Manually exporting and storing registration data introduces risks related to data consistency, accuracy, and compliance with data protection regulations. The lack of standardized, automated data flows increases vulnerability to errors and potential breaches.

- **Process Transparency & Monitoring Gaps**  
  There is limited visibility into the real-time status of the training process. Without centralized tracking, it's difficult to monitor progress, identify bottlenecks, or report reliably on process performance.

- **Tool Fragmentation & Siloed Systems**  
  The use of disconnected tools such as Pimcore, Outlook, Inxmail, CAS, Excel, and Share creates fragmented workflows. Data does not flow seamlessly between systems, leading to duplication of effort and increased reliance on manual coordination.

- **Limited Reusability & Standardization**  
  Key process elements—like email templates, registration forms, and certificate generation—lack standardization. Each new training setup often requires recreating similar components from scratch, resulting in inefficiencies and inconsistent participant experiences.

# To-Be Process
- **Scope and focus** PLACEHOLDER --> Clearly outline areas where we focused and how they positivly impact the identified process challenges

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

## Process: Training Scheduling

![Training Scheduling BPMN](https://github.com/user-attachments/assets/d65b3f20-d0be-4b4e-95bd-e772b466aca2)

### Start Event
The training scheduling process can be initiated either manually or at a defined interval (e.g., every 3 months). Automating the process start based on a time-triggered event allows for regular outreach to lecturers and ensures that new training dates are proactively offered.

---

### User Task: Update Calendly Event Types
The process begins with the GWP coordinator updating Calendly Event Types. Calendly is used to collect availability from lecturers, with each training topic assigned to a specific event type.
![image](https://github.com/user-attachments/assets/afa8d6a7-6686-447f-912f-13d9ba754263)

Before proceeding, the coordinator ensures:
- All relevant training sessions are listed,
- Availability restrictions (e.g., holidays, blocked times) are respected.

As this is a user task, Camunda prompts the coordinator to confirm that all event types are up to date before continuing.
![image](https://github.com/user-attachments/assets/28cd95a2-64d5-4bd9-8f5c-8d1ea67d02da)

---

### User Task: Choose Training Topic
The coordinator selects one of three available training topics offered by GWP. This selection is passed as a process variable and will determine which event types and lecturers are targeted in the following step.
![image](https://github.com/user-attachments/assets/057497c3-040d-4492-8bb0-c66e53ede8d0)

---

### Service Task: Send Link to Lecturers
This step is executed via Make.com, triggered by a Camunda webhook. It performs the following:

![Make Scenario – Send to Lecturers](https://github.com/user-attachments/assets/e6608544-1625-494c-9b72-bfccc943053a)

1. **Webhook Trigger:** Activated by Camunda, sending the selected training topic.
2. **Google Sheets – Search Rows:** Looks up registered lecturers from a CRM sheet.
3. **Iterator:** Breaks the results into individual lecturer entries.
4. **Calendly – List Event Types:** Fetches all active training slots.
5. **Filter "SelectEventType":** Matches the topic to the correct event type.
6. **Calendly – Create Single-Use Link:** Generates a unique booking URL per lecturer.
7. **Gmail – Send Email:** Delivers personalized emails to each lecturer.
![Instructor email availability sample](https://github.com/user-attachments/assets/f21c5f30-2e7d-4740-976a-7fdc9e4c56dd)
8. **Webhook Response:** Sends an “OK” back to Camunda.

---

### Intermediate Event: Wait for 7 Days
This timer event introduces a 7-day pause, giving lecturers time to respond. It's implemented as a Camunda timer event, but the delay duration is fully configurable.

---

### Service Task: Check Received Answers
This scenario continuously runs in Make.com, monitoring for incoming bookings and logging responses in a CRM Google Sheet:
![Make Scenario – Monitor Answers]<img width="848" alt="image" src="https://github.com/user-attachments/assets/557d80d4-7869-441a-9fc4-243b68dc5d24" />

1. **Calendly – Watch Events / List Event Invitees**
2. **Google Sheets – Add a Row:** New responses are added to the CRM with a `"Processed"` column set to `"No"`.
3. **Google Sheets – Search & Update:** Avoids duplicates and updates entries when necessary.

This setup ensures responses are continuously captured and marked for further processing.

---

### Service Task: Evaluate Lecturer Responses
After 7 days, Camunda triggers this Make scenario to assess whether any new responses exist:

![Make Scenario – Evaluate Responses](<img width="836" alt="image" src="https://github.com/user-attachments/assets/fc41b8cb-ebb6-4870-90ed-7c004d6b2d3b" />)

1. **Webhook Trigger:** Starts when Camunda proceeds past the timer event.
2. **Google Sheets – Search Rows:** Filters entries with `"Processed" = No"`.
3. **Array Aggregator & Set Variable:** Compiles relevant data and sets the `rowsFound` variable using:  
   `{{if(length(28.array) > 0; "true"; "false")}}`
4. **Webhook Response:** Sends `rowsFound` back to Camunda.

---

### XOR Gateway: Received Answers from Lecturer?
This exclusive gateway checks the value of the `rowsFound` process variable:

- `${rowsFound == true}` → Continue to **Decide on Lecturer**
- `${rowsFound == false}` → End process (no response received)

Implemented natively in Camunda, this decision gate ensures the process only proceeds when responses are available, maintaining efficiency.

---

### Service Task: Decide on Lecturer
This service task is implemented via Make.com and is responsible for selecting the best available lecturer based on participant ratings and availability.
<img width="827" alt="image" src="https://github.com/user-attachments/assets/48b142e3-011a-4445-bd3c-e84f93236372" />


**Process Logic:**

1. **Webhook Trigger:** Camunda sends a webhook call to Make.com.
2. **Google Sheets – Clear Staging Sheet:**  
   The `updateWebsite` sheet is cleared to ensure no stale or leftover data interferes with the current run.
3. **Google Sheets – Search Rows:**  
   Searches the `ProvidedAvailability` sheet for entries marked as `"Processed" = No"` and sorts them by **User Rating** (0–5 scale).
4. **Array Aggregator – Rank by Rating:**  
   Sorts the lecturers by rating and selects the top entry as the preferred instructor.
5. **Google Sheets – Add to Staging Sheet:**  
   Writes the selected lecturer’s information into the `updateWebsite` sheet. This will later be used to update the registration site.
6. **Webhook Response to Camunda:**  
   Sends a 200-OK to Camunda so the process can continue.
7. **Google Sheets – Update Processed Flags:**  
   All entries used in the selection process are updated to `"Processed" = Yes"` to avoid reprocessing in future executions.

## PLACEHOLDER - STILL MISSING TO BE CONTINUED JC

<img width="266" alt="image" src="https://github.com/user-attachments/assets/f08c6d05-b225-4e51-a845-90a623868e1a" />


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

## Process "Training Completion Processing":

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


<img width="573" alt="image" src="https://github.com/user-attachments/assets/2b05cb18-5a54-438e-b3fa-0a84f3346f99" />

### If attendance is not given, send an email to the non-attendee:
<img width="1322" alt="image" src="https://github.com/user-attachments/assets/45a01a8e-01bc-44a7-acb9-95d6d61bdbb6" />

This process is triggered by a custom webhook and handles participants whose attendance could not be confirmed. It searches the CRM registration sheet for entries where the attendance field is empty or not marked with “Yes”. For each non-attendee, an automated email is sent via Gmail. The message informs them that their attendance could not be verified, and kindly asks them to contact the GWP team. 

<img width="1177" alt="image" src="https://github.com/user-attachments/assets/cf46da90-deac-48fc-a2d2-c274549cfcbb" />

# Technologies used 
| Technology | Purpose |
| ------------- |------------------------------------
| Camunda 7 | Workflow automation and BPM execution |
| BPMN 2.0 | Visual language for modeling business processes |
| Make | No-code automation for apps and workflows |
| Cursor | 
| Google Sheets |


# Outlook



