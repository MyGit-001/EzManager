# EzManager - Digital Contact Management System

## 📖 Introduction
EzManager is a centralized web-based Contact Management System designed for organizing, coordinating, and managing personal and professional contacts efficiently[cite: 2]. This application provides a seamless user experience with responsive design, cross-device compatibility, and robust backend security[cite: 2].

## ✨ Features
The system supports distinct user roles (Admin and User) with the following core functionalities[cite: 2]:

*   **Secure Authentication:** User login, signup, and logout functionalities secured by Spring Security (`MyConfig.java`, `UserDetailsServiceImpl.java`, `CustomUserDetails.java`) to ensure authentication, authorization, and role-based access control[cite: 2].
*   **Add Contacts:** Users can create new contacts by inputting details such as name, workplace, location, phone number, description, and a profile picture (`add_contact_form.html`)[cite: 2].
*   **View & Search:** Users can browse a comprehensive list of their saved contacts (`show_contacts.html`) and utilize a custom `SearchController` to quickly find specific individuals[cite: 2].
*   **Update Contacts:** Seamless updating of contact information via dedicated update forms (`update_form.html`) to maintain an accurate digital recordbook[cite: 2].
*   **Delete Contacts:** Users can safely remove outdated or irrelevant contacts to maintain data integrity[cite: 2].
*   **User Profile Management:** Users can manage their account settings (`settings.html`), update passwords, and change their profile pictures from the user dashboard (`user_dashboard.html`)[cite: 2].

## 🛠️ Tech Stack
*   **Backend:** Java, Spring Boot, Spring Security, Maven (`pom.xml`)[cite: 2]
*   **Frontend:** HTML5, CSS3, JavaScript, Bootstrap, Thymeleaf (Templates located in `src/main/resources/templates`)[cite: 2]
*   **Database:** MySQL[cite: 2]
*   **Architecture:** MVC (Model-View-Controller)[cite: 2]

## 🚀 Getting Started (Local Setup)

### Prerequisites
Before you begin, ensure you have the following installed on your local machine:
*   Java Development Kit (JDK) 11 or higher
*   Maven (or use the included `mvnw` / `mvnw.cmd` wrapper)[cite: 2]
*   MySQL Server
*   Any Java IDE (IntelliJ IDEA, Eclipse, VS Code)

### Installation Steps

1. **Clone the repository:**

        git clone https://github.com/your-username/EzManager.git
        cd EzManager

2. **Database Configuration:**
   * Create a new MySQL database for the application.
   * Open the `src/main/resources/application.properties` file[cite: 2].
   * Update the database connection properties with your MySQL database URL, username, and password.

3. **Build and Run the Application:**
   * You can run the application directly from your IDE by executing the `SmartcontactmanagerApplication.java` file[cite: 2].
   * Alternatively, use the provided Maven wrapper[cite: 2] in your terminal:

        ./mvnw spring-boot:run

4. **Access the Application:**
   * Open your web browser and navigate to `http://localhost:8080`

## 🏗️ System Architecture & Code Structure
The application follows a systematic, top-down MVC design pattern[cite: 2]:

*   **Frontend (View):** The user interface built with Bootstrap, custom CSS (`style.css`), and Thymeleaf[cite: 2]. Templates are organized into public views (`home.html`, `login.html`, `signup.html`) and secure user views inside the `normal` directory[cite: 2].
*   **Controllers:** Handle routing and business delegation (`HomeController.java`, `UserController.java`, `SearchController.java`)[cite: 2].
*   **Entities (Model):** Java classes representing database tables (`User.java`, `Contact.java`)[cite: 2].
*   **Repository (DAO):** Manages data access and persistence, extending Spring Data JPA (`UserRepository.java`, `ContactRepository.java`)[cite: 2].
*   **Helpers:** Utility classes for handling application messages (`Message.java`)[cite: 2].

## 🗄️ Database Design
The system utilizes a relational database model structured around two primary entities with a bidirectional mapping[cite: 2]:

*   **User Entity:** Attributes include `user_id` (Primary Key), `name`, `password`, `role` (Admin/User), and `image`[cite: 2].
*   **Contact Entity:** Attributes include `contact_id` (Primary Key), `name`, `work_at`, `description`, and `image`[cite: 2].
*   **Relationships:** 
    *   **One-to-Many:** Each `User` can have multiple `Contact` entities[cite: 2].
    *   **Many-to-One:** Each `Contact` is associated with exactly one `User`[cite: 2].

## 📸 Screenshots
*(Add screenshots of your application here by replacing the placeholder links)*
*   [Login/Signup Page](#)
*   [User Dashboard](#)
*   [Add Contact Form](#)
*   [View Contacts List](#)

## 📌 Project Scope & Assumptions
*   **Performance:** Designed to handle a large volume of contacts without performance degradation[cite: 2].
*   **Security:** Data is securely protected from unauthorized access, utilizing session management and encrypted credentials[cite: 2].
*   **Scalability:** The architecture accommodates future growth of the contact database[cite: 2].
