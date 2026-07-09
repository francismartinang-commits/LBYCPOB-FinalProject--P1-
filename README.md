# PROJECT TITLE
Hospital/Lab Information System

## TEAM MEMBERS
Paragas, Nash Breann C.- Nash Paragas

Ang, Francis Martin B. - Tin Ang

Balingit, Joshua Andrei B. - Jandrei-cpe

### PROBLEM STATEMENT & GOALS
To design, develop, and implement an Object-Oriented Medical and Laboratory Information System that streamlines patient care, automates clinical and laboratory workflows, and provides secure, role-based access to health data. 

- To centralize patient and doctor identification along with their personal information and records
- To automate transition from visitation and consultation to a targeted Doctor Recommendation
- To enforce role-based access control (Admins, Doctors, Patient UI)
- To have a centralized access to clinical documentation and medical papers
- To enable real-time specimen tracking
- To Automate Intelligent Laboratory Request Routing 


### TARGET USER
The target users and beneficiaries of the Hospital Information System are the people involved in the hospital:

- Patients - Allows them join space with doctors and get updates from processes.
- Doctors - Transfer updates and results in an organized way. 
- Laboratory Staff - Reduce unclear requests and allows them to encode findings 
- Staff - Traceability of patient and updates
- Administrators - Monitor the flow of the entire hospital

### BRIEF DESCRIPTION
<Summary of purpose and basic functionality>

### CORE OOP CONCEPTS <br>

#### Abstraction

Abstraction will be used by creating general classes that represent the main parts of the Hospital/Lab Information System.

##### Possible abstract or general classes include: 
- User/Patient
- Doctor/Medic
- LaboratoryTest 
- MedicalRecord 

##### Ex:
- User/Patient - name, ID
- Laboratory Test - test name, specimen type, status

#### Encapsulation

Encapsulation will be used to protect sensitive patient and medical information by keeping class attributes private and only reachable through public methods (getters and setters) that check the requester's role before returning or changing anything. 

Possible applications:
- Patient - personal information, medical history (private fields, restricted getters)
- MedicalRecord - diagnosis, doctor's notes, findings (private fields, visible only to the assigned doctor or the patient)
- Visit - currentStatus (private field, changeable only through a validated method)
- User (any role) - username, password (private, never directly exposed to other classes)
- GUI - to hide unnecessary information and functions of the program

#### Inheritance

Inheritance will be used to build a hierarchy for the different types of system users. The abstract User/Patient class already identified under Abstraction can serve as a general parent class, with each specific role inheriting its shared attributes and methods, then adding its own specialized fields and behaviors. 

Possible utilization for this are
- User (Parent/Base class) - shared attributes (userID, name, username, password) and shared methods (login(), logout())
- Child classes: Patient, Doctor, Nurse/Staff, Laboratory Staff, Admin - each inherits the base User fields/methods, then extends them

#### Polymorphism

Polymorphism will be used to allow a single method name or action to behave differently depending on the object or data inputs being used. This will be implemented through method overriding (same method name with different behaviors per user role) and method overloading (same method name with different parameters).

Possible polymorphic actions or behaviors include:
- displayDashboard() (Method Overriding)
- createRequest() (Method Overloading)
- updateStatus() (Method Overriding)

##### Example:
- displayDashboard()
- Doctor Object - displays assigned patients, clinical assessment fields, and laboratory order forms.
- Laboratory Staff Object - displays pending specimen queues, routing tracking, and findings encoding sheets.
- createRequest()
- createRequest(String testName) - processes a single, standard laboratory request.
- createRequest(String[] testNames, String priority) - processes a bundled batch of tests flagged with a specific priority level (e.g., Urgent/Stat).

### INITIAL CLASS IDEAS:
- User (Abstract class for general user info like Name, ID, and Role)
- Patient (Subclass of User to hold patient medical history and current visit status)
- Doctor (Subclass of User to manage assigned patients and write assessment notes)
- LabRequest (Class to track the test name, specimen status, and laboratory findings)

### USER STORIES (Recommended):
- As a Patient, I want to track the real-time status of my lab sample so that I know exactly when my results will be ready.
- As a Doctor, I want to create a laboratory request directly from my dashboard so that the lab staff can see it immediately without manual paperwork.
- As a Laboratory Staff member, I want to encode test findings into the system so that the doctor can review them right away.

### CORE FEATURES (Recommended):
- Role-Based Access Control: A secure login system that shows a different dashboard interface depending on whether the user is an Admin, Doctor, Nurse, Lab Staff, or Patient.
- Real-Time Visit Lifecycle Tracker: A step-by-step workflow tracking system that automatically updates a patient's status from "Registered" all the way to "Released".
- Intelligent Lab Request Routing: A feature that sends doctor-made lab requests straight to the correct laboratory section for analysis and allows fast-track encoding of test results.


## Example Picture:

![Test Image](https://i.imgur.com/5jY0YUn.jpeg)
![Test Image](https://i.imgur.com/wweElPN.jpeg)
![Test Image](https://i.imgur.com/h6eTfUW.jpeg)
