# 🚌 University Bus Tracking System

### Smart University Transport Tracking & Management Portal

A Java-based web application developed for **SRM University-AP** that helps students track their allocated university buses, view estimated arrival times, receive arrival alerts, and find alternative buses when they miss their scheduled bus.

The system provides a centralized transport portal with live bus tracking, student eligibility verification, and an administration dashboard.

---

## 🌟 Project Overview

Students often depend on fixed bus timetables without knowing the actual bus location or arrival time. Our system solves this problem by providing a digital platform for tracking university buses and managing transport operations.

The application currently supports TN-2, TN-3, and TN-4 routes with simulated GPS tracking.

## ✨ Key Features

- 🗺️ **Live Bus Tracking** – Track bus locations on an interactive Leaflet map.
- ⏱️ **Estimated Arrival Time (ETA)** – Calculate approximate arrival times based on distance and speed.
- 🔔 **Arrival Alerts** – Receive notifications 5, 10, or 15 minutes before bus arrival.
- 🚌 **Alternative Bus Finder** – Find other buses serving the same boarding stop.
- 🔐 **Student Eligibility Verification** – Restrict access based on transport enrolment, fee payment, and bus allocation.
- 👨‍💼 **Admin Dashboard** – Manage students, buses, drivers, routes, and allocations.
- ⚙️ **GPS Simulation Controls** – Start, pause, adjust speed, and simulate bus delays.
- 👤 **Role-Based Access** – Separate student and administrator functionality.

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| Java 17 | Core programming language |
| Spring Boot 3.3.4 | Backend framework |
| MySQL 8+ | Primary database |
| SQLite | Automatic database fallback |
| Redis | Session and in-memory storage |
| HTML, CSS, JavaScript | Frontend |
| Leaflet.js | Interactive maps |
| Server-Sent Events (SSE) | Live tracking updates |
| Web Audio API | Arrival alarm sounds |
| Maven | Build and dependency management |
| JUnit 5 & Mockito | Testing |

## 🏗️ System Architecture

The application follows a layered architecture:

1. **Client Layer:** Student and administrator browser interfaces.
2. **Web Layer:** REST controllers, security filters, and event streaming.
3. **Service Layer:** Authentication, tracking, ETA calculation, alerts, and alternative bus services.
4. **Data Layer:** JDBC-based database access using MySQL with SQLite fallback.
5. **External Services:** Mock university transport API and simulated GPS engine.

## 🔄 Application Workflow

1. Student selects an account from the login portal.
2. The system verifies transport eligibility.
3. A secure session is created.
4. The student dashboard displays allocated bus information.
5. Live GPS simulation updates the bus location.
6. ETA and arrival alerts are calculated.
7. Students can find alternative buses if they miss their allocated bus.

## 📂 Project Structure

```text
University-Bus-Tracking-System/
│
├── java__project/
│   └── bus-tracking/
│       ├── src/
│       │   ├── main/
│       │   │   ├── java/
│       │   │   └── resources/
│       │   └── test/
│       ├── data/
│       ├── docs/
│       ├── tools/
│       ├── pom.xml
│       └── docker-compose.yml
│
├── README.md
├── University Bus Tracking System video presentation.mp4
└── University Bus Tracking system 008 Report..pdf
```

## 🚀 Getting Started

### Prerequisites

- Java 17 or later
- Maven (or the included Maven Wrapper)
- MySQL 8+ (if using the primary database)
- Redis (if using the Redis session store)

### Installation

**1. Clone the repository**

```bash
git clone https://github.com/rithikasundari/University-Bus-Tracking-System.git
```

**2. Navigate to the project directory**

```bash
cd University-Bus-Tracking-System/java__project/bus-tracking
```

**3. Configure the application**

Check the application configuration and `.env.example` file. Set up the required database and Redis settings.

**4. Build the project**

Windows:

```powershell
.\mvnw.cmd clean package
```

**5. Run the application**

```powershell
.\mvnw.cmd spring-boot:run
```

Open the local application URL configured by the project.

## 🧪 Testing

The project uses JUnit 5 and Mockito for testing.

Run the test suite:

```powershell
.\mvnw.cmd test
```

The project includes tests for authentication, database rules, alternative bus services, and application eligibility scenarios.

## 📊 Testing Results

| Metric | Result |
|---|---:|
| Tests executed | 22 |
| Failures | 0 |
| Errors | 0 |
| Test classes | 3 |
| Demo login scenarios | 9 |

## 🎥 Project Demo

Watch the project demonstration video:

**University Bus Tracking System – Video Presentation**

[View Demo Video](./University%20Bus%20Tracking%20System%20video%20presentation.mp4)

## 📄 Project Documentation

The complete project report is available here:

[View Project Report (PDF)](./University%20Bus%20Tracking%20system%20008%20Report..pdf)

## ⚠️ Important Notes

- GPS tracking currently uses simulated location updates, not physical GPS hardware.
- Student records and transport information are synthetic demo data.
- The university transport API is mocked for demonstration.
- Google sign-in is optional; demo mode is the default.
- Database and session storage have fallback mechanisms.

## 🔮 Future Enhancements

- Integration with real GPS devices.
- Connection to the actual university transport API.
- Push notifications and SMS alerts.
- Support for additional bus routes and stops.
- Enhanced security and performance improvements.

## 👥 Team Members

**Group 008 – SRM University-AP**

- Siddy Rithika Sundari
- Dintakurthi V N S Lakshmi Rishitha
- D. Vennela
- Galla Sruthi
- Syam Kumar Yata

---

## 🎓 Academic Project

Developed as a university-level Java project to demonstrate object-oriented programming, Spring Boot, database connectivity, real-time event streaming, and web application development.

**Made by Team Group 008 | SRM University-AP**
