# EzManager - Digital Contact Management System

## 📖 Introduction
EzManager is a centralized web-based Contact Management System designed for organizing, coordinating, and managing personal and professional contacts efficiently. This application provides a seamless user experience with responsive design, cross-device compatibility, and robust backend security.

## ✨ Features
The system supports distinct user roles (Admin and User) with the following core functionalities:

*   **Secure Authentication:** User login, signup, and logout functionalities secured by Spring Security (`MyConfig.java`, `UserDetailsServiceImpl.java`, `CustomUserDetails.java`) to ensure authentication, authorization, and role-based access control.
*   **Add Contacts:** Users can create new contacts by inputting details such as name, workplace, location, phone number, description, and a profile picture (`add_contact_form.html`).
*   **View & Search:** Users can browse a comprehensive list of their saved contacts (`show_contacts.html`) and utilize a custom `SearchController` to quickly find specific individuals.
*   **Update Contacts:** Seamless updating of contact information via dedicated update forms (`update_form.html`) to maintain an accurate digital recordbook.
*   **Delete Contacts:** Users can safely remove outdated or irrelevant contacts to maintain data integrity.
*   **User Profile Management:** Users can manage their account settings (`settings.html`), update passwords, and change their profile pictures from the user dashboard (`user_dashboard.html`).

## 🛠️ Tech Stack
*   **Backend:** Java, Spring Boot, Spring Security, Maven (`pom.xml`)
*   **Frontend:** HTML5, CSS3, JavaScript, Bootstrap, Thymeleaf (Templates located in `src/main/resources/templates`)
*   **Database:** MySQL
*   **Architecture:** MVC (Model-View-Controller)

## 🚀 Getting Started (Local Setup)

### Prerequisites
Before you begin, ensure you have the following installed on your local machine:
*   Java Development Kit (JDK) 11 or higher
*   Maven (or use the included `mvnw` / `mvnw.cmd` wrapper)
*   MySQL Server
*   Any Java IDE (IntelliJ IDEA, Eclipse, VS Code)

### Installation Steps

1. **Clone the repository:**

        git clone https://github.com/your-username/EzManager.git
        cd EzManager

2. **Database Configuration:**
   * Create a new MySQL database for the application.
   * Open the `src/main/resources/application.properties` file.
   * Update the database connection properties with your MySQL database URL, username, and password.

3. **Build and Run the Application:**
   * You can run the application directly from your IDE by executing the `SmartcontactmanagerApplication.java` file.
   * Alternatively, use the provided Maven wrapper in your terminal:

        ./mvnw spring-boot:run

4. **Access the Application:**
   * Open your web browser and navigate to `http://localhost:8080`

## 🏗️ System Architecture & Code Structure
The application follows a systematic, top-down MVC design pattern:

*   **Frontend (View):** The user interface built with Bootstrap, custom CSS (`style.css`), and Thymeleaf. Templates are organized into public views (`home.html`, `login.html`, `signup.html`) and secure user views inside the `normal` directory.
*   **Controllers:** Handle routing and business delegation (`HomeController.java`, `UserController.java`, `SearchController.java`).
*   **Entities (Model):** Java classes representing database tables (`User.java`, `Contact.java`).
*   **Repository (DAO):** Manages data access and persistence, extending Spring Data JPA (`UserRepository.java`, `ContactRepository.java`).
*   **Helpers:** Utility classes for handling application messages (`Message.java`).

## 🗄️ Database Design
The system utilizes a relational database model structured around two primary entities with a bidirectional mapping:

*   **User Entity:** Attributes include `user_id` (Primary Key), `name`, `password`, `role` (Admin/User), and `image`.
*   **Contact Entity:** Attributes include `contact_id` (Primary Key), `name`, `work_at`, `description`, and `image`.
*   **Relationships:** 
    *   **One-to-Many:** Each `User` can have multiple `Contact` entities.
    *   **Many-to-One:** Each `Contact` is associated with exactly one `User`.

## 📸 Screenshots
*(Add screenshots of your application here by replacing the placeholder links)*
*   [Login/Signup Page](#)
*   [User Dashboard](#)
*   [Add Contact Form](#)
*   [View Contacts List](#)

## 📌 Project Scope & Assumptions
*   **Performance:** Designed to handle a large volume of contacts without performance degradation.
*   **Security:** Data is securely protected from unauthorized access, utilizing session management and encrypted credentials.
*   **Scalability:** The architecture accommodates future growth of the contact database.
