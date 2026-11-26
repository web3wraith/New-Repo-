1. Project Overview
   
1.1 Product Name:<br>
MyHealth.web (an Electronic Health Records (EHR) Management System).

1.2 Product Description<br>
MyHealth.web is a centralized digital platform designed to manage, store, and provide secure access to patients' medical records across multiple healthcare facilities.
The system aims to eliminate the challenges associated with fragmented and paper-based medical records by providing a unified platform where patient information can be accessed and updated by authorized healthcare professionals, regardless of the participating hospital a patient visits.
Through the platform, patients will be able to manage their medical profiles, view their medical histories, book appointments, access prescriptions, and receive laboratory results. Doctors will be able to retrieve patient records, document consultations, prescribe medications, request laboratory investigations, and make referrals.
The system will also provide hospital administrators with tools for managing staff accounts, assigning roles, and controlling access to medical information.
By integrating these functionalities into a single platform, MyHealth.web seeks to improve medical record accessibility, streamline healthcare processes, enhance information sharing between hospitals, and promote continuity of patient care.

1.3 Project Vision<br>
To establish a unified healthcare information system that makes patient medical records accessible, secure, and transferable across participating healthcare facilities, irrespective of where patients receive medical attention.

1.4 Project Goal<br>
To develop a centralized Electronic Health Records system that simplifies patient record management, improves communication between healthcare professionals and facilities, and supports more efficient and informed healthcare delivery.

2. Problem Statement<br>

The clinic is slow because records are either searched for manually, lost and there is no appointment system, so students wait long and repeat themselves every visit.

3. Business Objectives

What does the business want?<br>1. Reduce waiting time by 50% through online booking.<br>2. Reduce lost files to zero by storing records digitally.<br>3. Improve follow-up care by keeping full patient history.<br>4. Help the clinic make faster and safer decisions.

4.**Target users**<br>
-Primary users: Students<br>
-Secondary users: Health Workers (doctors, nurses)<Br>
- Secondary users: Laboratories<br>

5.**Stakeholders**<br>
-Students<br>
-Health workers<br>


6.**User Stories**<br>

-As a student, i want to book appointments online so i don't have to wait over an hour at the clinic to get my treatment (58.3% - 14/24 responders requested this).<br>
-As a student, i want to access lab results easily without coming back to the clinic to get it (62.5% - 15/24 responders requested this).<br>
-As a student i want to access my medical records easily to avoid repeating the same process each time i visit the clinic (50% - 12/24 responders requested this).<br>
-As a student, I want a drug prescription and drug reminder feature so I don't miss my drugs. (50% - 12/24 responders requested this feature).<br>
-As a student, I want to chat with medical personnel so I can ask quick questions. (50% - 12/24 responders requested this feature).<br>
-As a student, I want to have access control of my medical record, so that my privacy is protected. (58.3% - 14/24 responders requested this feature).<br>

7. **Functional Requirements**:<br>Must have: Student registration page and login page with matric number and student email<br>
Must have: Online appointment scheduling, cancelling, and viewing (This solves 47.8% of long wait periods when visiting the clinic).<br>
Must have: Digital Medical records that can be easily retrieved by students' matric number (This solves 62.5% of medical records retrieval failures.<br>
Must have: Viewing lab results for students<br>
Must have: Explicit consent prompt: students must approve a medical professional before medical records can be opened<br>
Should have: Drug prescription and reminder feature.<br>
Should have: Emergency contact and ambulance request.<br>
Can have in call/messaging feature to chat with medical personnel.


8. **Non-Functional Requirements**:<br>
Privacy: System must have role based access and an explicit consent prompt.  Students must approve before medical records can be opened. (33.3% of responders requested this).<br>
Security: Encryption of passwords, session timeout, and an audit log of viewing records activities must be put in place  (25.0% of responders requested this).<br>
Performance: Appointments must be booked in less than 2 minutes. Medical records must be retrieved in seconds.<br>
Offline performance: system should store data offline through offline caching and sync when network is back online.<br>

Metrics source: https://docs.google.com/forms/d/e/1FAIpQLSfz_m7zweLjkm6N9uv1Z1eA_2M4IF5s7ePBIq6O9EVuE3z7ag/viewform?usp=header

9. **Scope and Priorities - Phase 1**:<br>

**Privacy and Safety(Main Features)**

**Different Logins and Accessibility**: Separate accounts for patients, nurses, doctors etc., that shows each side what they are allowed and need to see.

**Data Protection and Activity History**: Prevents outsiders or non medical personnel from getting access to private medical info, and displays a history log showing who opened, edited, sent a file etc.

**Patient Permission Control**: Grants the patient the ability to allow or block a clinic, personnel or unwanted individuals access to their medical history.


**Medical Record/Info**

Patient's Basic Info: Shows the name, unique ID number(after registration), age, gender, weight, height, blood type, genotype, close contacts(In case of emergencies), health insurance details(if any).

Vitals: A place where medical personnel can write down the blood pressure, temperature, heart rate, weight etc. based on tests that have been conducted.

Health Background/History: Shows all records pertaining to past medical reports such as ongoing conditions(diabetes, asthma etc.), allergies(if any), past surgeries and family health history.

Doctor Visit Notes: A form that shows the reason why a patient visits, test and check-up details(blood pressure, temperature etc.), diagnosis and recommended treatment plan.

Digital Prescriptions and Test requests: Allows doctors to create drug prescriptions and lab test slips that patients can view and download on their device.


**Client and Patient Tasks(Sub Feature)**

Booking: A calendar that allows the patient or user the ability to book, view and cancel appointment plans.

Test Result Uploads: Allows lab staff or patients to upload photo or PDF files of test results into a patient's health folder for easy access.


**Basic Health Checker(Sub Feature)**

Daily Health Tracker: A place for patients to type in their blood pressure, blood sugar, and weight to track changes and receive health recommendations and tips.

Basic Symptom Quiz: A simple step-by-step questionnaire where patients can select symptoms that they are currently experiencing and how bad they feel that tells gives the user safe advice(Rest at home, Book a doctor etc.) based on the collated results of the questionnaire.



**Future Releases - Phase 2**

Virtual Care: Video/Audio Consultations( Telemedicine), In-app messaging, Automated reminders.

Online payment gateways.

AI and advanced tech: Ai powered symptom analysis, Smartwatch or wearable device syncing.

Clinic Billing and Invoicing.



10.**Acceptance Criteria**

User accounts and security

•	Role Separation: A user logged in as a patient can only view their own medical records and cannot access Doctor or medical personnel dashboards.

•	Data Encryption: All passwords are encrypted in the database, and the site loads strictly over HTTPS.	

•	Activity Logging: Every time a doctor opens or edits a patient's file, the system automatically records the doctor's name, date, and exact time in an audit log.


**Patient Digital Profile**

•	Unique ID Generation: Submitting the registration form creates a unique id automatically for the patients and prevents duplicate accounts using the same number or email.

•	Mandatory Fields: The system prevents form submission and displays error messages if required details such as name, gender, age etc. are left blank.


**Basic Health Checker**

•	Rule Based Triage: Selecting high risk symptoms such as "Chest pain + Difficulty breathing", triggers the "Seek immediate Emergency Care" warning or response.

•	Booking Link for a clinic: Completing the quiz with moderate symptoms displays a working "Book an appointment/doctor" button that takes the patient to the appointment screen.


**Medical Records**

•	Clinical Notes: Doctor's can save a visit note for a patient to view which cannot be deleted but saved and updated with a timestamp, for medical history integrity.

•	PDF Prescriptions: "Generate Prescription" button creates a clean, downloadable PDF that contains the clinic's name, doctor's signature/ID, diagnosis, prescribed medication and dosage and date.

•	Health Records: Health history and medical records of a patient are permanently stored in the database for access if the patient grants it.


**Basic Appointment Booking**

•	Double-Booking Prevention: As soon as a patient books a doctor's time ( e.g 11am) for a particular clinic, that time slot immediately becomes unavailable for all other patients.

•	Notification: Booking an appointment automatically sends a confirmation email or SMS to the patient immediately.


9.**ASSUMPTIONS AND OPEN QUESTIONS**<br>
**Assumptions**<br>
**User and Behavioral Assumptions**<br>
Digital - Literacy:  Patients and healthcare workers should have the basic smartphones or computer literacy required to navigate the interface without extensive step-by-step guidance because they feel they cannot do a task.<br>
Language & Medical terms Comprehension:  Patients must be able to  accurately understand the medical terms or symptoms questions presented to them without them finding it difficult due to language barrier.<br>
Patient Trust & Willingness to Share: Patients are willing to input accurate, sensitive health data (including stigmatized conditions) into a digital system rather than withholding it for the fear of being exposed.<br>
Self-Reporting Accuracy: Patients must be able to accurately describe their symptoms, timelines, and severity without exaggerating or missing critical clinical signs.<br><br>

 **Infrastructure & Technical Assumptions**<br>
Reliable Connectivity & Power: Clinics and patients should have consistent access to internet data and electricity.<br>
Device Availability: Healthcare facilities already possess—or can afford to procure and maintain—tablets, laptops, or reliable smartphones at every point of care.<br>

 **Clinical & Operational Assumptions**
Workflow Alignment: Health workers will find typing or clicking through digital forms faster—or at least more valuable—than scribbling in physical paper folders during high-volume clinic hours.<br>
Diagnostic & Triage Safety: The symptom checker algorithm is accurate enough to flag emergencies (red flags) without causing unnecessary panic (false positives) or giving false reassurance (false negatives).<br>
Standardized Medical Coding: Clinics use consistent naming conventions for drugs, lab tests, and diagnoses (e.g., ICD-10), rather than informal shorthand.<br>

**Business, Legal & Regulatory Assumptions**
Data Privacy Compliance: The system should be able to complies with local data protection laws and patients must be able to trust that their medical records will not be leaked.<br>
Liability & Clinical Governance: You have clear legal boundaries clarifying that the "Health Checker" provides informational triage, not a definitive medical diagnosis, protecting you from medical malpractice claims.<br>
Willingness to Pay: Either patients , private clinics/hospitals , or HMOs/insurers see enough immediate financial or time-saving value to pay for the software sustainably.<br>


**Open-Questions**<br><br>
**Costumer and Income Question**<br>
Who is the true buyer?: Will private hospital owners pay for a B2B subscription, will HMOs sponsor it to reduce fraudulent claims, or will patients pay per consultation.<br>
What is the profit for a clinic?:  Does the software help a hospital make more money (e.g., faster HMO billing) or save money (e.g., preventing lost paper files and drug theft), or is it just a waste?.<br>
How do you compete with "free"?: WhatsApp, and basic Excel sheets cost almost nothing. Why would a clinic/health organization switch to your  paid system?, or will there be a free trial for a certain period of time?.<br>
**Technical Questions**<br>
What happens when the internet or power goes out?: Can a nurse still admit a patient, record vitals, and prescribe drugs offline and does the data sync when the network returns?<br>
Who owns the patient's record?:If a patient visits a clinic  in the rural area and later goes to a clinic in the urban area , can they carry their digital record with them, or does the clinic in the rural area lock that data inside their own account?<br>
How will old paper records be migrated?: Do clinics start fresh from Day 1, or do they expect you to digitize thousands of existing physical folders?.<br>

**Clinical and Patient behavior Questions**<br>
Will doctors input the information manually during consultations?:In a busy clinic where one doctor sees 40+ patients a day, will they actually enter notes into the system or will they write on paper and make an assistant type it later?<br>
How do patients react to the System?: Will patients trust an automated symptom checker, or will they bypass it due to their lack of information to demand talking to a real doctor immediately?<br>
What happens when symptoms are vague?: How accurately can the system handle facial expressions of symptoms (e.g.”Pimples”, “heat reactions") without giving dangerous triage advice?<br>

**Regulatory and Informational Questions**<br>
If the Health Checker tells a patient their chest pain is "mild indigestion" and it turns out to be a heart emergency, who is legally responsible?<br>
When information is leaked due to a patient’s mistake or the system's mistakes?:How do you determine who is responsible or do you just brush it off if the patient isn’t aware of it?<br>




