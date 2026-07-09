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
<Who will use this system?>

### BRIEF DESCRIPTION
<Summary of purpose and basic functionality>

### CORE OOP CONCEPTS

#### Abstraction

Abstraction will be used by creating general classes that represent the main parts of the Hospital/Lab Information System.

##### Possible abstract or general classes include: 

User/Patient

Doctor/Medic

LaboratoryTest 

MedicalRecord 

##### Ex:

User/Patient - name, ID

Laboratory Test - test name, specimen type, status

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
- ClassName1: <responsibility>
- ClassName2: <responsibility>
- ClassName3: <responsibility>

### USER STORIES (Recommended):
- As a <user type>, I want to <action> so that <goal>.
- As a <user type>, I want to <action> so that <goal>.

### CORE FEATURES (Recommended):
- <Feature 1>
- <Feature 2>
- <Feature 3>

## Example Picture:

![Test Image]([https://i.imgur.com/RcVBZeD.jpeg](https://www.pinterest.com/pin/713609503492935714/))
