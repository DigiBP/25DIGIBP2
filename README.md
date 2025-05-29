## Table of Contents

- [Introduction📥](#introduction-)
- [Team Members👥](#team-members-)
- [Coaches🧑‍🏫](#coaches-)
- [AS-IS Process🚩](#as-is-process-)
  - [1. Training Planning and Coordination](#1-training-planning-and-coordination)
  - [2. Registration Page and Promotion](#2-registration-page-and-promotion)
  - [3. Participant Registration and Confirmation](#3-participant-registration-and-confirmation)
  - [4. Pre-Training Preparation](#4-pre-training-preparation)
  - [5. Training Delivery and Attendance Tracking](#5-training-delivery-and-attendance-tracking)
  - [6. Training Completion Processing](#6-training-completion-processing)
  - [7. Self-Study for No-Shows](#7-self-study-for-no-shows)
- [BPMN Diagram – AS-IS Training Process at GWP🚩](#bpmn-diagram-as-is-training-process-at-gwp)
- [Project Goals 🏁](#project-goals)
  - [Process Participant Roles 🔍](#process-participant-roles)
  - [Identified Challenges in the AS-IS Process🚧](#identified-challenges-in-the-as-is-process)
- [Scope and Process Improvement Focus Areas🎯](#scope-and-process-improvement-focus-areas)
- [TO-BE Process Implementation🚀](#to-be-process-implementation)
  - [Process 1: Training Scheduling🗓️](#process-1-training-scheduling)
  - [Process 2: Participant Registration📝](#process-2-participant-registration)
  - [Process 3: Training Completion Processing🎓](#process-3-training-completion-processing)
- [Technologies Used🛠️](#technologies-used)
- [Next Steps in the Digital Journey🔮](#next-steps-in-the-digital-journey)

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
| Juan-Camilo Ramírez | 
| Anaïs von Dach | 
| Micaela Palma Costa | 

# Coaches 🧑‍🏫
| Name               |
|--------------------|
| Andreas Martin     |
| Charuta Pande      |
| Devid Montecchiari |

 
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


## BPMN Diagram – AS-IS Training Process at GWP🚩
![GWP As-Is Process Diagram](https://github.com/user-attachments/assets/49a511e7-c2d6-4595-92b5-492dc0883cf5)

> The above BPMN diagram visualizes the current end-to-end training process, highlighting key manual touchpoints and tool handoffs across planning, registration, delivery, and certification stages. The focus of this group will be on the processes highlighted in green: Training Scheduling, Participant Registration, and Training Completion Processing


[Download the complete AS-IS BPMN file HERE](./Documents/As-Is%20Process/AS-IS%20Training%20Process%20at%20GWP.bpmn)

# Project Goals :checkered_flag:

The primary goal of this project is to improve the efficiency, scalability, and transparency of GWP’s training program by digitizing and partially automating the end-to-end process—from planning to certificate issuance. Based on the challenges identified in the current (as-is) process, the project focuses on the following objectives:
 
- Enhance Operational Efficiency
- Increase Process Automation
- Improve Data Consistency and Compliance
- Strengthen Participant Experience
- Increase Transparency and Monitoring
 
## Process Participant Roles🔍
- GWP – Coordinating entity (Advisor for financial service providers)
- Participants – course attendees
- Lecturer – the course facilitators

## Identified Challenges in the AS-IS Process🚧 
The current training process at GWP, while structured, presents several challenges that limit efficiency, scalability, and consistency. The following issues have been identified:

### 🔄 Process Execution Challenges

- **Manual Work & Workflow Disruptions**  
  Many process steps rely on manual handling and switching between tools. Tasks such as managing incoming registration emails or exporting and saving participant lists are time-consuming and error-prone. These media disruptions increase the likelihood of mistakes and slow down execution.
  
- **Communication Delays**  
  Coordination between GWP, lecturers, and participants—particularly around setting and confirming training dates—often involves several rounds of back-and-forth communication. This leads to delays in publishing registration materials and complicates scheduling.

- **Limited Reusability & Standardization**  
  Key process elements—like email templates, registration forms, and certificate generation—lack standardization. Each new training setup often requires recreating similar components from scratch, resulting in inefficiencies and inconsistent participant experiences.

---

### 🧩 System & Tooling Limitations

- **Tool Fragmentation & Siloed Systems**  
The use of disconnected tools such as Pimcore, Outlook, Inxmail, CAS, Excel, and Share creates fragmented workflows. Data does not flow seamlessly between systems, and limited integration options prevent meaningful automation. This not only increases administrative overhead but also restricts the ability to scale the process as training demand grows.

---

### 🔐 Data & Compliance Risks

- **Data Handling Issues**  
  Manually exporting and storing registration data introduces risks related to data consistency, accuracy, and compliance with data protection regulations. The lack of standardized, automated data flows increases vulnerability to errors and potential breaches.

- **Process Transparency & Monitoring Gaps**  
  There is limited visibility into the real-time status of the training process. Without centralized tracking, it's difficult to monitor progress, identify bottlenecks, or report reliably on process performance.
  

## Scope and Process Improvement Focus Areas🎯

As part of the initial wave of GWP’s digitalization initiative, we focused on automating three key end-to-end processes within the training lifecycle:

1. 🗓️ **Training Scheduling**  
2. 📝 **Participant Registration**  
3. 🎓 **Training Completion Processing**

These three processes were selected based on their **high impact on administrative workload, process delays, and data integrity** — and their direct connection to the core challenges identified in the AS-IS analysis. Each improvement is designed to reduce manual workload, eliminate redundancies, increase process transparency, enhance real-time visibility, while establishing a scalable and integrated architecture supported by automation. These three processes align along the end-to-end training lifecycle at GWP:

![Training Process Overview and Value Stream](https://github.com/user-attachments/assets/2399c2b9-cf0b-4fed-aa1a-a2d85052b9e7)

---

### 🗓️ 1. Training Scheduling

- Use of Forms as a user interface to interact with lecturers and collect availability data  
- Elimination of manual back-and-forth communication via email or chat by using [Calendly](https://calendly.com/)  
- Grouping of related coordination tasks to improve efficiency and visibility

**🔗 Addressed Challenges:**  
- **Manual Work & Workflow Disruptions**, by digitizing initial coordination steps  
- **Communication Delays**, by introducing structured data collection  
- **Tool Fragmentation**, through Google Sheets CRM, Calendly, and Make.com integration
---

### 📝 2. Participant Registration

- After successful registration, the system updates a central Google Sheet (CRM layer) and validates entries in real time  
- Registered participants automatically receive a confirmation email with the Microsoft Teams link  
- CRM integration ensures that participants not yet in the system are automatically added

**🔗 Addressed Challenges:**  
- **Manual Work**, by automating communication and CRM updates  
- **Tool Fragmentation**, by consolidating registration tracking in one source  
- **Data Handling Issues**, by ensuring consistent, compliant participant records

---

### 🎓 3. Training Completion Processing

This process encompasses all post-registration and post-delivery activities, including preparation support for instructors, attendance validation, certificate generation, and non-attendee follow-up.

#### 🎥 Training Delivery Support
- Pre-structured and automatically exported registration lists are generated prior to the session.
- This supports instructor preparation and reduces manual effort in assembling participant data.

#### 🧾 Certificate Creation
- Automatic comparison of MS Teams attendance logs with the registration list  
- Certificates are generated and emailed automatically

#### ⏯️ Non-Attendee Handling
- Non-attendees are automatically identified and excluded from certificate generation  
- A dedicated notification is sent requesting they contact the GWP coordinator

**🔗 Addressed Challenges:**  
- **Manual Work**, by replacing ad hoc list management and document handling  
- **Process Transparency**, by ensuring instructors and the system have timely, accurate data  
- **Limited Reusability & Standardization**, through consistent logic for attendance and certification  
- **Data Handling Issues**, via structured registration exports and validated attendance input

# TO-BE Process Implementation🚀

## Process 1: Training Scheduling🗓️

![Training Scheduling BPMN](https://github.com/user-attachments/assets/d65b3f20-d0be-4b4e-95bd-e772b466aca2)

---

### 🧱 Foundational Data Layer: Google Sheets CRM

A dedicated **CRM database built in Google Sheets** serves as the backbone of the entire digitalized workflow. It provides a consistent, persistent data model that supports integrations across Forms, registration, attendance tracking, and certificate generation. This centralization ensures data quality, reduces duplication, and enables scalable automation across the entire training lifecycle.

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

![Make Scenario – Monitor Answers](https://github.com/user-attachments/assets/557d80d4-7869-441a-9fc4-243b68dc5d24)

1. **Calendly – Watch Events / List Event Invitees**
2. **Google Sheets – Add a Row:** New responses are added to the CRM with a `"Processed"` column set to `"No"`.
3. **Google Sheets – Search & Update:** Avoids duplicates and updates entries when necessary.

This setup ensures responses are continuously captured and marked for further processing.

---

### Service Task: Evaluate Lecturer Responses
After 7 days, Camunda triggers this Make scenario to assess whether any new responses exist:

![Make Scenario – Evaluate Responses](https://github.com/user-attachments/assets/fc41b8cb-ebb6-4870-90ed-7c004d6b2d3b)

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
![Make Scenario – Decide_on_lecturer](https://github.com/user-attachments/assets/48b142e3-011a-4445-bd3c-e84f93236372)


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

### User Task: Check Updated Website
After selecting the lecturer and updating the website staging sheet, the process pauses for manual verification. The GWP coordinator must confirm that the live registration website reflects the latest data.

1. **Camunda Form Task:** The form contains a single checkbox. The GWP coordinator is responsible for manually verifying the website before checking the box.
2. **Verification Scope:** The coordinator compares the following fields displayed on the live website against the values in the `updatedWebsite` sheet in Google Sheets:
   - Training Name  
   - Lecturer First Name  
   - Lecturer Last Name  
   - Start Date  
   - Start Time  
   - End Date  
   - End Time
3. **Completion Condition:** If any discrepancies are found, the coordinator must address them before checking the box and allowing the process to continue.

![Camunda Form – Check Updated Website](https://github.com/user-attachments/assets/0bfb7b4a-8164-41a3-87c2-49d1c2da2b2f)

> The registration site is deployed on Vercel. Further technical details on content updates will be provided in a later section.

---

### Service Task: Send Link to Participants
This step is executed via Make.com, triggered by a Camunda webhook. It performs the following:

![Make Scenario – Send Link to Participants](https://github.com/user-attachments/assets/dd16fb60-5ca4-446d-9809-c63c049feb51)



1. **Webhook Trigger:** Activated by Camunda to start the participant outreach workflow.
2. **Google Sheets – Search Rows:** Looks up email addresses from the `Customer_Data` CRM sheet, using the `Email` field.
3. **Gmail – Send an Email:** Delivers personalized emails to each potential participant. The email includes a registration link to the Vercel-hosted training site.
![Email_sent_to_potential_participants](https://github.com/user-attachments/assets/511d9ff5-800f-4ad8-b007-8f74c94697d4)
4. **Webhook Response:** Sends an “OK” back to Camunda, confirming successful execution.

---

### End Event: Training Offer Published
Once the email has been sent to all potential participants, the BPMN process concludes with a **None End Event** in Camunda, indicating that the training offering has been successfully published and promoted.

---

### 📂 Access the Implementation Files

All implementation assets for the *Training Scheduling* process are available in the repository, including:

- The BPMN model and Camunda forms  
- The Make.com automation scenario (JSON export)  
- A mock Google Sheets-based CRM workbook

➡️ [Browse files for Process 1](./Documents/To-Be%20Process/process-1-training-scheduling)


These resources provide a complete view of how the scheduling process was orchestrated, automated, and integrated.


## Process 2: Participant Registration📝
![TO-BE Process – Participant Registration](https://github.com/user-attachments/assets/847e7da2-9c36-4887-b403-053fcbfcab2b)

---

### 🌐 Foundational Participant Interaction Layer: GWP Training Registration Website

To enable participants to register for GWP’s training courses, a dedicated **GWP Training Registration Website** has been developed. It serves as the primary user interface for external participants, allowing them to browse available courses and register via a clean, mobile-optimized form.

A short video demo of the website can be viewed here:  
🔗 [Watch on YouTube](https://youtu.be/g6MmasZI31U)

#### Key Features

- **Dynamic Course Information Display** – Course details are fetched in real time from a connected Google Sheets data source.
- **Responsive Registration Form** – A mobile-friendly modal interface with input validation ensures smooth form completion across devices.
- **Google Sheets Integration** – Submissions are written directly into the CRM layer using Google Apps Script, eliminating the need for a backend server.
- **Corporate Design** – The site follows GWP’s branding guidelines to ensure visual consistency with other touchpoints.

#### Architectural Highlights & Benefits

1. **Serverless Architecture** – Built using Google Apps Script for data handling, with no dedicated backend infrastructure required.
2. **Simple Maintenance** – Course content and availability can be updated directly in Google Sheets by GWP staff.
3. **Responsive Design** – Optimized for desktop, tablet, and mobile viewing.
4. **Brand Integration** – Fully aligned with GWP’s corporate design standards.
5. **Global Hosting** – Deployed via **Vercel**, leveraging a global CDN for fast, reliable access.

---

To keep this documentation focused on the process level, the full technical architecture (including code snippets and configuration logic) is provided in the expandable block below:

<details>
  <summary>▶️ View full website integration code and architecture </summary>

  ```text
### Technical Architecture:

## Frontend (Vercel-hosted)

- Static HTML/CSS/JavaScript
- Responsive design with mobile support
- Deployed on Vercel's global CDN

## Backend (Google Apps Script)

- Web App endpoint for data operations
- Google Sheets for data storage
- No traditional server required

## Frontend Components


# HTML Structure

Deployment URL
The application is accessible at: https://gwp-registration-8zh0reb8w-moritzs-projects-ed6c1909.vercel.app/

Deployment Process
1. Vercel automatically builds and deploys the static site
2. Global CDN ensures fast loading times
3. Automatic HTTPS certificate management
4. Environment variables can be set in the Vercel dashboard if needed


The main page includes:

<header>
    <div class="container">
        <div class="logo">
            <img src="https://www.gwp.ch/layout/logo/gwp_logo-plain.svg" alt="GWP Logo">
        </div>
        <nav>
            <ul>
                <li><a href="index.html">Training 2025</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </nav>
    </div>
</header>

<main>
    <section class="hero">
        <!-- Hero content -->
    </section>

    <section class="courses">
        <div class="container">
            <h2>Available Courses</h2>
            <div class="course-grid" id="courseList">
                <!-- Course items loaded via JavaScript -->
            </div>
        </div>
    </section>

    <!-- Registration Modal -->
    <div id="registrationModal" class="modal">
        <!-- Registration form -->
    </div>
</main>

<section id="contact">
    <!-- Contact information and map -->
</section>

# Contact Section

The contact section displays:

<section id="contact">
  <div class="contact-container">
    <div class="contact-info">
      <img src="https://www.gwp.ch/layout/logo/gwp_logo-plain.svg" alt="gwp logo">
      <div>Bleicherweg 72 - 8002 Zürich</div>
      <div>+41 44 221 91 00</div>
      <div>
        <a href="mailto:zurich@gwp-group.com">zurich@gwp-group.com</a>
      </div>
      <div>
        <a href="https://www.gwp.ch/de/home" target="_blank">www.gwp.ch/de/home</a>
      </div>
    </div>
    <div class="contact-map">
      <iframe
        src="https://www.google.com/maps?q=Bleicherweg+72,+8002+Zürich,+Switzerland&output=embed"
        width="100%" height="350" style="border:0; border-radius: 8px;" allowfullscreen="" loading="lazy">
      </iframe>
    </div>
  </div>
</section>


# Registration Form

The registration form collects:

- First and Last Name
- Company
- Email
- Address, Postcode, City
- Course information (automatically populated)

<form id="registrationForm">
    <div class="form-group">
        <label for="firstName">First Name</label>
        <input type="text" id="firstName" name="First_Name" required>
    </div>
    <!-- Other form fields... -->
    <input type="hidden" id="courseName" name="Course_Name">
    <input type="hidden" id="courseDate" name="Course_Date">
    <div class="form-group">
        <button type="submit" class="submit-button">Submit Registration</button>
    </div>
    <div class="loading-spinner" id="loadingSpinner"></div>
</form>



## Google Sheets Integration

# Integration Flow
1. Course Data Display: GET request to fetch course information to Spreadsheet tab "updateAvalability"
2. Registration Submission: POST request to store registration data "Anti-Money Laundering (AML)_Registration Data"
3. Validation & Feedback: Response handling for user notification

# Google Sheets Integration Code

const APPS_SCRIPT_URL = 'https://script.google.com/macros/s/AKfycbyCYq9J38ckend7yWCEDSlQ6J-uUQ3uBVfNrhn8TgEHu2btO71GmQ6l-GZJAKSV5y4w0Q/exec';

// Define the exact fields we want to collect and save
const ALLOWED_FIELDS = [
  'First_Name',
  'Last_Name',
  'Company',
  'Email',
  'Address',
  'Postcode',
  'City',
  'Course_Name',
  'Course_Date'
];

// Main function to send form data to Google Sheets
function sendFormData(formData) {
  // Filter the form data to only include allowed fields
  const filteredData = {};
  ALLOWED_FIELDS.forEach(field => {
    if (formData[field] !== undefined) {
      filteredData[field] = String(formData[field]).trim();
    }
  });
  
  // Send data to Google Apps Script endpoint
  return new Promise((resolve, reject) => {
    // Convert data to URL encoded format
    const formBody = Object.entries(filteredData)
      .map(([key, value]) => encodeURIComponent(key) + '=' + encodeURIComponent(value))
      .join('&');
    
    fetch(APPS_SCRIPT_URL, {
      method: 'POST',
      headers: {
        'Content-Type': 'application/x-www-form-urlencoded'
      },
      body: formBody
    })
    .then(response => response.json())
    .then(data => {
      // Handle success response
      if (data.status === 'success') {
        resolve({
          success: true,
          message: data.message || 'Registration submitted successfully!'
        });
      } else {
        reject(new Error(data.message || 'Unknown error from server'));
      }
    })
    .catch(error => {
      // Handle error and try fallback method if needed
      console.error('Error sending form data:', error);
      // Fallback mechanism code...
    });
  });
}



# Fetching Course Data

function fetchCourseAvailability() {
  return fetch(APPS_SCRIPT_URL)
    .then(response => {
      if (!response.ok) {
        throw new Error(`HTTP error ${response.status}`);
      }
      return response.json();
    })
    .then(data => {
      if (data.status === 'success') {
        return data.data;
      } else {
        throw new Error(data.message || 'Failed to fetch course availability');
      }
    });
}



# Form Validation System

function processFormSubmission(formData) {
    // Show loading state
    document.getElementById('submit-button').disabled = true;
    document.getElementById('submit-button').innerText = 'Submitting...';
    
    submitViaGoogleAppsScript(formData)
        .then(response => {
            console.log('Submission successful:', response);
            
            // Reset the form
            document.getElementById('registration-form').reset();
            
            // Show success message
            const successBanner = document.getElementById('success-message');
            successBanner.style.display = 'block';
            
            // Scroll to the success message
            successBanner.scrollIntoView({ behavior: 'smooth' });
            
            // Hide the form
            document.getElementById('registration-form-container').style.display = 'none';
        })
        .catch(error => {
            // Error handling
            console.error('Submission error:', error);
            
            // Show error message
            const errorBanner = document.getElementById('error-message');
            errorBanner.style.display = 'block';
            errorBanner.innerText = 'There was an error submitting your registration.';
            
            // Scroll to the error message
            errorBanner.scrollIntoView({ behavior: 'smooth' });
        })
        .finally(() => {
            // Reset button state
            document.getElementById('submit-button').disabled = false;
            document.getElementById('submit-button').innerText = 'Submit';
        });
}



## Google Apps Script (Backend)

The Google Apps Script handles two main functions:

# Data Retrieval (GET Requests)

function doGet(e) {
  try {
    const availabilityData = getCourseAvailability();
    return ContentService.createTextOutput(JSON.stringify({
      status: "success",
      data: availabilityData
    })).setMimeType(ContentService.MimeType.JSON);
  } catch (error) {
    return ContentService.createTextOutput(JSON.stringify({
      status: "error",
      message: error.message
    })).setMimeType(ContentService.MimeType.JSON);
  }
}



# Registration Processing (POST Requests)

function doPost(e) {
  try {
    // Parse data from request
    let data = {};
    
    if (e && e.parameter && Object.keys(e.parameter).length > 0) {
      data = e.parameter;
    }
    else if (e && e.postData && e.postData.contents) {
      // Parse JSON data...
    }
    
    // Validate required fields
    const requiredFields = ['First_Name', 'Last_Name', 'Email', 'Course_Name'];
    for (const field of requiredFields) {
      if (!data[field]) {
        throw new Error(`Missing required field: ${field}`);
      }
    }
    
    // Map course to correct sheet
    const courseToSheet = {
      'Anti-Money Laundering (AML)': {
        sheetName: 'Anti-Money Laundering (AML)_Registration Data'
      },
      'Fraud Detection & Prevention': {
        sheetName: 'Fraud Detection & Prevention_Registration Data'
      },
      'Financial Advisory': {
        sheetName: 'Financial Advisory_Registration Data'
      }
    };
    
    // Get the sheet info for the selected course
    const courseInfo = courseToSheet[data.Course_Name];
    if (!courseInfo) {
      throw new Error(`Invalid course name: "${data.Course_Name}"`);
    }
    
    // Get the correct sheet and append data
    const ss = SpreadsheetApp.openById('1WmBn3Ye9WfuGenYQ0D6tWf1aeE1bcCbDTvCyYntHL-Y');
    const sheet = ss.getSheetByName(courseInfo.sheetName);
    
    // Append data to sheet...
    sheet.appendRow([
      data.First_Name || '',
      data.Last_Name || '',
      data.Company || '',
      data.Email || '',
      data.Address || '',
      data.Postcode || '',
      data.City || '',
      data.Course_Name || '',
      data.Course_Date || '',
      new Date().toISOString()
    ]);
    
    // Return success response
    return ContentService.createTextOutput(JSON.stringify({
      status: "success",
      message: "Registration submitted successfully"
    })).setMimeType(ContentService.MimeType.JSON);
    
  } catch (error) {
    // Return error response
    return ContentService.createTextOutput(JSON.stringify({
      status: "error",
      message: `Error processing registration: ${error.message}`
    })).setMimeType(ContentService.MimeType.JSON);
  }
}


```
</details>

---

### Start Event
This process is triggered in parallel with **Process 1: Training Scheduling**, either manually or via a scheduled time-based trigger (e.g., every 3 months). Launching both processes concurrently ensures that participant-facing workflows (like registration and CRM updates) are prepared in sync with lecturer coordination and training offer publication.

---

### Intermediate Event: Wait for 8 Days
This timer event introduces a delay before participant data is processed. It allows sufficient time for **Process 1** to complete lecturer selection and update the public registration website. The delay is configurable; in this case, an **8-day buffer** ensures that participant registrations are only processed once the website is up to date and active.

---

### Service Task: Check Received Answers
This task is executed via Make.com and triggered by a Camunda webhook. It checks whether new participant registrations have been received and prepares the data for further processing.

![Make Scenario – Check Received Answers](https://github.com/user-attachments/assets/73abdf4a-23ed-4554-92e5-e7b2689ce4d9)

**Process Logic:**

1. **Webhook Trigger:** Activated by Camunda when registrations open.
2. **Google Sheets – Search Rows:** Looks up new registered participants based on website form submissions.

![Google Sheet CRM - Registered participants snip](https://github.com/user-attachments/assets/e5f76c9a-918c-43f3-9598-a864001494df)

3. **Google Sheets – Update a Row:** Transfers confirmed registration data (e.g. for Anti-Money Laundering training) into the `Customer_Data` sheet and generates a new participant ID.

![Update Registration Row](https://github.com/user-attachments/assets/17d64144-58cd-47a7-b76f-802def06e7c1)

4. **Webhook Response:** Sends an “OK” back to Camunda to confirm task completion.

---

### Service Task: Send Confirmation Link
After a participant has successfully registered, this task sends a confirmation email with the Microsoft Teams meeting link. The process is fully automated to ensure timely delivery.

![Make Scenario – Send Confirmation Link](https://github.com/user-attachments/assets/bbadac4b-0dc9-48b5-b164-fc4f3861cc23)

**Process Logic:**

1. **Webhook Trigger:** Activated by Camunda.
2. **Google Sheets – Search Rows:** Confirms that the participant's `Registration Successful` column is marked `"Yes"`.

![Search Registered Rows](https://github.com/user-attachments/assets/62820053-0c8d-4d68-bdfa-a9326b3878f7)

3. **Gmail – Send Email:** Sends a personalized confirmation email including the Microsoft Teams meeting link.

![Email Module – Send Confirmation](https://github.com/user-attachments/assets/d8f198d9-a1dd-432f-afdc-9ef8eb8e51cc)
![Sample Email Content](https://github.com/user-attachments/assets/0642c5c2-12e7-4594-a306-786990727e28)

4. **Webhook Response:** Sends an “OK” back to Camunda.

---

### Service Task: Check and Register Participant in CRM
In this step, the system verifies whether the participant already exists in the CRM (Google Sheets). If the participant is not found, they are automatically added.

![Make Scenario – Check Participant in CRM](https://github.com/user-attachments/assets/f14c42b0-e8fe-4dbd-bc0f-00f1364ecfa2)

**Process Logic:**

1. **Webhook Trigger:** Activated by Camunda.
2. **Google Sheets – Search Rows:** Retrieves the participant from the `Anti-Money Laundering` sheet.
3. **Google Sheets – Search Rows:** Checks for a matching email address in the `Customer_Data` sheet.
4. **Router – Evaluate Email Match:**
   - If no match is found:  
     `{ "participantRegistered": false }` → Google Sheets – **Add Row** (register participant).
   - If a match is found:  
     `{ "participantRegistered": true }` → No action required.
5. **Webhook Response:** Sends `"true"` or `"false"` back to Camunda based on the participant’s CRM status.

---

### End Event: Participant Registered
Once the confirmation email has been sent and the CRM has been updated (if needed), the process concludes with a **None End Event** in Camunda, signaling that the participant registration workflow is complete.

---

### 📂 Download Implementation Assets

The following repository folder contains all artifacts for *Participant Registration*, including:

- BPMN model for Camunda  
- Make.com scenario for automated confirmations
  
_Note: The code for the registration website is included as a collapsable section in itself, therefore to avoid redundancy, it is not present in the folder referenced below_

➡️ [View files for Process 2](./Documents/To-Be%20Process/process-2-participant-registration)

These components illustrate how the registration flow was automated and connected to our CRM layer.


## Process 3: Training Completion Processing🎓

![Process 3 – Training Completion BPMN](https://github.com/user-attachments/assets/09a86e8a-5623-429b-b1c9-60f9169ab139)

---

### Start Event
This process is triggered based on the **End Date and Time** of the training session, as stored in the Google Sheets CRM. Once the scheduled end time is reached, the workflow is initiated to process participant completion, issue certificates, and handle non-attendance follow-up.

---

### User Task: Upload Attendance List from Teams Meeting
After the training session concludes, the GWP coordinator manually exports the **Microsoft Teams attendance report** and pastes it into a predefined Google Sheets format. This action serves as a trigger for the next automation step.

![Attendance Upload](https://github.com/user-attachments/assets/8e50535e-f342-4fee-a91a-34d095b89916)

---

### Service Task: Check Attendance Against CRM

![Make Scenario – Check Attendance](https://github.com/user-attachments/assets/fb381bc9-ece3-4acd-ad7a-70493bcbb9b4)

Once the attendance list has been uploaded, a **Make.com scenario** is triggered. It compares the entries in the uploaded list with the participants in the CRM registration sheet.

**Process Logic:**

1. **Google Sheets – Search Rows:** Retrieves registered participants.
2. **Google Sheets – Compare Attendance:** Matches Teams attendees to CRM entries.
3. **Google Sheets – Update Row:** If a match is found, marks `"Attendance"` as `"Yes"` in the CRM.

> Note: Due to limited Microsoft Teams permissions, this process remains **semi-automated** — manual upload is required to initiate the matching process.

![CRM Update – Attendance Status](https://github.com/user-attachments/assets/d8186c8a-7ad1-4d0f-955e-aebece7dccb0)

---

### Parallel Gateway: Process Attendees and Non-Attendees
Once the CRM is updated, the process continues in two parallel paths: one for issuing certificates to confirmed attendees, and another for notifying participants whose attendance could not be confirmed.

---

### Service Task: Issue Certificate and Send by Email

![Make Scenario – Send Certificate](https://github.com/user-attachments/assets/ff99c80b-100a-41cb-aa35-54391519770e)

This Make scenario is triggered by a custom webhook. It searches the CRM for participants marked with `"Yes"` in the attendance column and sends them a certificate.

**Process Logic:**

1. **Google Sheets – Search Rows:** Looks up participants with `"Attendance" = Yes"`.
2. **PDF Generator API – Create PDF:** Generates personalized certificates based on template and participant data.
3. **Gmail – Send Email:** Delivers the certificate as a PDF attachment to each attendee.

![Certificate Generator](https://github.com/user-attachments/assets/48f7388e-5879-424d-a3f0-d39af12aa808)
![Email Sent to Attendee](https://github.com/user-attachments/assets/2b05cb18-5a54-438e-b3fa-0a84f3346f99)

---

### Service Task: Inform Non-Attendees

![Make Scenario – Inform Non-Attendees](https://github.com/user-attachments/assets/45a01a8e-01bc-44a7-acb9-95d6d61bdbb6)

Participants whose attendance status remains empty or does not equal `"Yes"` are notified via email.

**Process Logic:**

1. **Google Sheets – Search Rows:** Finds CRM entries without confirmed attendance.
2. **Gmail – Send Email:** Informs participants that their attendance could not be confirmed and invites them to reach out to the GWP team for further steps.

![Email to Non-Attendee](https://github.com/user-attachments/assets/cf46da90-deac-48fc-a2d2-c274549cfcbb)

---

### End Event: Completion Processed
The process concludes once both the certificate issuance and non-attendee notifications have been executed. The final **None End Event** in Camunda signals that the training session has been fully closed from an administrative standpoint.

---

### 📂 Explore Process Artifacts

All supporting materials for the *Training Completion Processing* workflow are stored in the following folder:

- Certificate logic in Camunda BPMN and forms
- Make.com automation workflows (JSON)  

➡️ [Access files for Process 3](./Documents/To-Be%20Process/process-3-training-completion-processing)

This resource bundle shows how completion, certification, and non-attendance handling were digitalized.

# Technologies used🛠️
| Technology | Purpose |
| ------------- |------------------------------------
| Camunda 7 | Workflow automation, process orchestration, and BPM execution |
| BPMN 2.0 | Visual language for modeling business processes |
| ChatGPT | Generative AI chatbot used as a copilot to problem solve, as reference, and to correct style & grammar |
| Calendly | Highly configurable scheduling automation platform with easy out of the box integrations |
| Make.com | No-code / Low Code automation for apps and workflows |
| Cursor | AI powered IDE designed to enhance developer productivity |
| Google Sheets | Web based spreadsheet application capable of basic scripting and integrations  |


## Next Steps in the Digital Journey🔮

While the current implementation delivers strong improvements in process efficiency, scalability, and participant experience, several opportunities remain to increase maturity of GWP's digital training operations:

- **Multi-Course Selection Logic**  
  The current setup supports only one training topic at a time due to Make.com's single-webhook limitation. Future iterations could incorporate a decision layer to handle course branching more dynamically — likely requiring a low-code or pro-code implementation layer.

- **Instructor Selection Enhancement**  
  While ratings-based prioritization works well for now, more advanced selection criteria (e.g. expertise matching, availability constraints, past performance) could be integrated. A DMN approach was explored but deemed unsuitable; implementing this would likely require Java or Python-based custom logic.

- **Automated Non-Attendee Re-Scheduling**  
  Today, non-attendees are notified manually. A future version could automatically trigger re-scheduling flows, including personalized links to repeat sessions or access to self-study materials (video, slides, test links).

- **Participant Self-Service Portal**  
  A central dashboard where participants could manage registrations, download certificates, or access training content would improve user autonomy and reduce administrative overhead.

- **Audit Trail & Logging Layer**  
  To improve transparency and compliance, especially in regulated contexts, a versioned audit log of process events and participant interactions could be maintained, possibly integrated into the CRM layer.

These enhancements would enable GWP to move closer to intelligent orchestration — and lay the foundation for scaling the platform to cover all of its remote offering




