**Introduction**
1. **Purpose of this document**
-The purpose of this document is to provide a comprehensive overview of the technical design, component details, and database design for the Contact Management System project. It aims to capture the scope of the project, outline the assumptions made during the design process, identify potential risks, and highlight any dependencies that may impact the successful implementation of the system. This document serves as a reference for developers, stakeholders, and project managers involved in the Contact Management System project.

2. **Project overview**
-A contact management system web project serves as a centralized platform for organizing, coordinating, and managing events efficiently. It typically consists of two main user roles: admin and user. The admin possesses overwhelming control and authority over the system, Admin has the authority over the user’s account.  While users has the ability to add new add contacts, view them, search for them and delete them. Let's delve into the purpose and functionality of each component within this system.

3. **Users Functions:**
> Login, Signup and Logout:
The user's login feature ensures secure access to the system, requiring authentication to prevent unauthorized access. Spring Security ensures the authentication, authorization 	and access control for the user.  Upon successful authentication, the user gains access to app privileges, enabling them to access their digital hub. Logout functionality 		terminates the admin's session, enhancing security by preventing unauthorized access in shared environments.

> Add Contact:
Users have the authority to add new contacts to the platform. This functionality involves inputting contact details such as name, work at, location, phone number, description, 	profile picture any other pertinent information.

> View Contact:
Users can browse through a comprehensive list of contacts available on the platform added by them. The user can also search for a specific contact he/she is looking for. This 		functionality provides user with feature of availability.

> Delete Contact:
In instances where a specific contact is no longer required or deemed irrelevant, the user can remove them from the platform. The delete contact functionality ensures that 		outdated or erroneous information is promptly eliminated, maintaining the platform's integrity, and enhancing user experience.

> Update Contact: 
In instances where a specific contact needs to be updated by the user. The update contact functionality ensures that outdated information is updated without any effort, 		maintaining the platform's integrity, and enhancing user experience.

4. **Solution Summary**
Scope
The scope of this web application project includes developing a user-friendly platform for users where they can manage their contacts. The application will have user registration and authentication, user profile management, an admin dashboard for managing contacts and  responsive design for cross-device compatibility and robust security measures. The project aims to deliver a comprehensive solution that provides a seamless user experience, scalability to manage a large user base, and adherence to industry standards. This web application facilitates the user with a common space where they can organize their contacts. 

5. **Assumptions**
	Here are some assumptions for a contact management system project:
	1.	The system will be able to handle a large number of contacts without performance issues.
	2.	Users will have consistent and reliable internet connectivity to access the system.
	3.	The system will be user-friendly and intuitive, with minimal training required for end-users.
	4.	The data entered into the system will be secure and protected from unauthorized access.
	5.	The system will be able to integrate with other software applications used by the organization.
	6.	The system will be able to handle international characters and formats for names and addresses.
	7.	The system will have a backup and recovery plan in place to protect against data loss.
	8.	The system will comply with relevant data privacy regulations.
	9.	The system will be scalable to accommodate future growth of the organization's contact database.
	10.	The system will have adequate technical support and maintenance resources available.

6. **Schematic Diagram**
The schematic diagram for a Contact Management web application built using Spring Boot, Bootstrap, HTML, CSS, JavaScript, and MySQL would include different components like the front-end interface designed with HTML, CSS, Bootstrap for a visually appealing layout. Thymeleaf has been used as a template engine. The interactive features would be implemented using JavaScript for dynamic functionality. Spring Boot would manage the back-end operations, connecting with the MySQL database for storing and retrieving contact information and user data. The diagram would highlight the seamless integration between these technologies to create a user-friendly and efficient managing system for users.

7. **System Design**
System design is the process of defining the elements of a system such as the architecture, modules and components, the different interfaces of those components and the data that goes through that system. It is meant to satisfy specific needs and requirements of a business or organization through the engineering of a coherent and well-running system. It implies a systematic approach to the design of a system. It may take a bottom- up or top-down approach, but either way the process is systematic wherein it takes into account all related variables of the system that needs to be created from the architecture to the required hardware and software, right down to the data and how it travels and transforms throughout its travel through the system.

8. **Proposed design**
 	1. Frontend: The user interface where users interact with the system. It includes login/logout forms, contact listing, and deletion interfaces. 
 	2. Controller: Receives incoming requests from the frontend, delegates tasks to the appropriate service, and returns responses. It handles authentication, authorization, and 		routing.
 	3. Service: Contains the business logic of the application. It coordinates data flow between the controller and the repository. It handles tasks like adding contacts, deleting contacts, and user authentication.
	4. Repository: Manages data access and persistence. It communicates with the database to perform CRUD operations (Create, Read, Update, Delete) for contacts and user data.
 	5. Database: Stores contacts and user data persistently. It can be a relational database like MySQL.

10. **Database Design**
Data Model : 
ER Diagram stands for Entity Relationship Diagram, also known as ERD, is a diagram that displays the relationship of entity sets stored in a database. In other words, ER diagrams help to explain the logical structure of databases. ER diagrams are created based on three basic concepts: entities, attributes and relationships.ER Diagrams contain different symbols that use rectangles to represent entities, ovals to define attributes and diamond shapes to represent relationships. At first look, an ER diagram looks very similar to the flowchart. However, ER Diagram includes many specialized symbols, and its meanings make this model unique. The purpose of ER Diagram is to represent the entity framework infrastructure.
                   
For a Digital management system, we are using a relational database model.
Tables:
1) User:
   - user_id (Primary Key)
   - name
   - password
   - role (Admin/User)
   - other relevant user details
2) Contact:
   - contact_id (Primary Key)
   - name
   - work At
   - Image
   - description
   - other relevant event details

10. **Relationships:**
   - Each user can have multiple contacts (One-to-Many relationship between User and contact).
   - Each contact is associated with one user (Many-to-One relationship between contact and User).

11. **Functions:**
    
- Login / Signup
   -- Verify user credentials against the User table.
- 	Logout
   -- End the user session.
- 	Add Contact
   -- Insert a new contact record into the contact table.
-	Update Contact
   -- Update an existing contact record into the contact table.
-	Delete Event
   -- Remove a contact record from the table based on contact obj.
-	User Settings
   -- A user can change or update his/her password in the setting, he can also update his profile picture.


	# EzManager - Digital Contact Management System

## 📖 Introduction
EzManager is a centralized web-based Contact Management System designed for organizing, coordinating, and managing personal and professional contacts efficiently[cite: 2]. This application provides a seamless user experience with responsive design, cross-device compatibility, and robust backend security[cite: 2].

## ✨ Features
The system supports distinct user roles (Admin and User) with the following core functionalities[cite: 2]:

*   **Secure Authentication:** User login, signup, and logout functionalities secured by Spring Security to ensure authentication, authorization, and role-based access control[cite: 2].
*   **Add Contacts:** Users can create new contacts by inputting details such as name, workplace, location, phone number, description, and a profile picture[cite: 2].
*   **View & Search:** Users can browse a comprehensive list of their saved contacts and utilize a search functionality to quickly find specific individuals[cite: 2].
*   **Update Contacts:** Seamless updating of contact information to maintain an accurate and current digital recordbook[cite: 2].
*   **Delete Contacts:** Users can safely remove outdated or irrelevant contacts to maintain data integrity[cite: 2].
*   **User Profile Management:** Users can manage their account settings, update passwords, and change their profile pictures[cite: 2].

## 🛠️ Tech Stack
*   **Backend:** Java, Spring Boot, Spring Security[cite: 2]
*   **Frontend:** HTML5, CSS3, JavaScript, Bootstrap, Thymeleaf (Template Engine)[cite: 2]
*   **Database:** MySQL[cite: 2]
*   **Architecture:** MVC (Model-View-Controller), RESTful routing[cite: 2]

## 🏗️ System Architecture
The application follows a systematic, top-down MVC design pattern to ensure clean separation of concerns[cite: 2]:

1.  **Frontend (View):** The user interface built with Bootstrap and Thymeleaf where users interact with the system (login forms, contact listings, etc.)[cite: 2].
2.  **Controller:** Receives incoming HTTP requests from the frontend, handles routing, and delegates business tasks[cite: 2].
3.  **Service Layer:** Contains the core business logic, coordinating data flow between the controllers and repositories[cite: 2].
4.  **Repository (DAO):** Manages data access and persistence, communicating with the database to perform CRUD operations[cite: 2].
5.  **Database:** A relational MySQL database for persistent storage[cite: 2].

## 🗄️ Database Design
The system utilizes a relational database model structured around two primary entities[cite: 2]:

**User Table**[cite: 2]
*   `user_id` (Primary Key)
*   `name`
*   `password`
*   `role` (Admin/User)
*   `image` / `other details`

**Contact Table**[cite: 2]
*   `contact_id` (Primary Key)
*   `name`
*   `work_at`
*   `description`
*   `image` / `other details`

**Relationships:**
*   **One-to-Many:** Each User can have multiple Contacts[cite: 2].
*   **Many-to-One:** Each Contact is associated with exactly one User[cite: 2].

## 📌 Project Scope & Assumptions
*   **Performance:** Designed to handle a large volume of contacts without performance degradation[cite: 2].
*   **Security:** Data is securely protected from unauthorized access, utilizing session management and encrypted credentials[cite: 2].
*   **Scalability:** The architecture accommodates future growth of the contact database[cite: 2].
*   **Accessibility:** Requires consistent internet connectivity and supports international character formats for global names and addresses[cite: 2].
