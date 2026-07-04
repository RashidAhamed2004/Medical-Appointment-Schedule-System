# Medical Appointment Scheduling System

A full-stack web application designed to streamline the process of scheduling and managing medical appointments. The system allows patients to register, login, view doctors, select time slots, and schedule appointments, while providing administrative interfaces to manage doctors, view user feedback, and handle system notifications.

---

## 🚀 Key Features

*   **User Authentication**: Register and login pages for patients and administrators.
*   **Appointment Booking**: Select preferred doctors, appointment dates, and time slots.
*   **Doctor Management**: Interfaces for administrators to view, add, and manage doctor records.
*   **Time Slot Scheduling**: Admin controls to set availability schedules for different doctors.
*   **Feedback & Notifications**: Real-time admin panels to read feedback and notifications from patients.
*   **File-Based Persistence**: Simple and efficient file-based storage for user accounts and appointments (stored as structured `.txt` files).

---

## 📁 Project Structure

```text
Medical-Appointment-Scheduling-System/
├── Back-end/                  # Spring Boot Java Application
│   ├── src/main/java/...      # Controllers, Models, and File Storage logic
│   ├── src/main/resources/    # Application configurations (application.properties)
│   ├── mvnw / mvnw.cmd        # Maven wrappers for quick builds without Maven preinstalled
│   └── pom.xml                # Project dependencies (Spring Starter Web, Test)
│
└── Front-end/                 # Client Web Application
    ├── login.html             # Login portal
    ├── Registration.html      # Patient registration page
    ├── Home.html              # Main application home page
    ├── bookAppointment.html   # Booking form for patients
    ├── doctorManagement.html  # Admin panel for doctor configuration
    ├── style.css              # Custom global styles
    └── *.js                   # Javascript logic handling API calls to the Back-end
```

---

## 🛠️ Tech Stack

*   **Back-end**: Java 21+ / Spring Boot 3.x / Maven
*   **Front-end**: HTML5 / Vanilla CSS3 / JavaScript (ES6 Fetch API)
*   **Data Storage**: Flat-file persistence (`.txt` database files)

---

## ⚙️ How to Run the Project

### 1. Running the Back-end (Spring Boot Server)

The back-end server runs on **port 8080** and handles all REST API requests.

#### Prerequisites:
*   Java JDK 21 or higher installed on your machine.
*   If you have IntelliJ-managed JDKs, you can use the path `C:\Users\rashi\.jdks\openjdk-24` as `JAVA_HOME`.

#### Steps:
1.  Open your terminal/command prompt.
2.  Navigate to the `Back-end` directory:
    ```bash
    cd Back-end
    ```
3.  Set the `JAVA_HOME` environment variable and run the application using the Maven wrapper:
    *   **PowerShell (Windows)**:
        ```powershell
        $env:JAVA_HOME="C:\Users\rashi\.jdks\openjdk-24"
        .\mvnw.cmd spring-boot:run
        ```
    *   **CMD (Windows)**:
        ```cmd
        set JAVA_HOME=C:\Users\rashi\.jdks\openjdk-24
        mvnw.cmd spring-boot:run
        ```
    *   **Linux / macOS**:
        ```bash
        export JAVA_HOME=/path/to/your/jdk
        ./mvnw spring-boot:run
        ```
4.  The server will start up, and its REST endpoints will be available at `http://localhost:8080/`.

---

### 2. Running the Front-end (Client UI)

Since the frontend is built using standard static HTML/CSS/JS, you have two options to run it:

#### Option A: Direct browser execution (Simple)
Simply navigate to the `Front-end` folder and double-click **`login.html`** or **`Home.html`** to open it directly in your web browser.

#### Option B: Local development server (Recommended)
To avoid any relative path restrictions and run it under a local port:
1.  If you have Node.js installed, serve the `Front-end` directory:
    ```bash
    cd Front-end
    npx http-server -p 3000
    ```
2.  Open your browser and navigate to `http://localhost:3000/login.html`.
3.  If you are using **VS Code**, you can also install the **Live Server** extension and click **Go Live** on any `.html` file inside the `Front-end` folder.

---

## 🐙 Git Workflow Guide

To add new changes and push them to your GitHub repository:

1.  **Check repository status**:
    ```bash
    git status
    ```
2.  **Add your changes**:
    ```bash
    git add .
    ```
3.  **Commit with a descriptive message**:
    ```bash
    git commit -m "Add README documentation and configure execution guidelines"
    ```
4.  **Push to GitHub**:
    ```bash
    git push origin main
    ```
