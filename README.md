# CityMove

**CityMove** is a Java‐based interactive application designed for University of Calgary students to : 
1. **Survey** and rate study spots on campus  
2. **Build and view** personalized class‐time schedules  

It ships in two flavours—**text‐based** (console) and **GUI**—and includes a suite of JUnit tests to ensure correctness.

*This work was conducted to fulfill the CPSC 233 course requirement at the University of Calgary*

---

## ✨ Features

- **User Accounts**  
  Sign up / log in with a username & password.  
  Credentials are stored in `UserAccounts.dat`.

- **Study-Spot Survey**  
  • Rate buildings, libraries, coffee shops, etc.  
  • Persist your ratings in `StudySpotsListV1.0.0.txt`.

- **My Schedule**  
  • View a week‐view of your classes (“yellow arrow” highlights current period).  
  • Data driven by the built-in `schedule.png` & `UofCMap.png` assets.

- **Two UIs**  
  1. **Console** (text) mode via the `Survey` driver  
  2. **Graphical** mode via the `Gui` driver (Swing-based)

- **Automated Testing**  
  • Unit tests for core logic (`StudySpotTest.java`, `StudySpotListTest.java`, `ScheduleTest.java`)  
  • Uses JUnit 4.12 + Hamcrest 1.3

---

## 📂 Repository Layout
```
CityMove/
├── account/                 # UserAccount model & persistence
│   └── Account.java
├── logic/                   # Core survey, schedule, and map logic
│   ├── SurveyLogic.java
│   ├── ScheduleLogic.java
│   └── StudySpotsListV1.0.0.txt
├── unitTests/               # JUnit test classes
│   ├── StudySpotTest.java
│   ├── StudySpotListTest.java
│   └── ScheduleTest.java
├── Gui.java                 # Swing-based GUI entry point
├── Survey.java              # Console-based entry point
├── Survey.jar               # (optional) bundled JAR for console mode
├── CityMove.jar             # (optional) bundled JAR for GUI mode
├── Logo.jpg                 # University of Calgary logo
├── UofCMap.png              # Campus map background
├── schedule.png             # Sample schedule template
├── YellowArrow.png          # Cursor icon for “current period”
├── star.png                 # Rating-star icon
└── UserAccounts.dat         # Stored user credentials
```


---

## 🚀 Getting Started

### Prerequisites

- Java 8 or newer  
- JUnit 4.12 + Hamcrest 1.3 (for running tests)

### 1. Clone the repo

```
bash
git clone https://github.com/KeatonBuddy/CityMove.git
cd CityMove
```
### 2. Compile all sources

```
bash
javac *.java account/*.java logic/*.java
```
### 3a. Run the console version
```
bash
java Survey
```
- S → Sign up (first‐run only)

- L → Log in

- S → Take the study‐spot survey

- C → View your schedule
  
### 3b. Run the GUI version
```
bash
java Gui
```
- Enter credentials and click Signup / Login

- Click Do Survey or My Schedule from the main menu

## 🧪 Running Tests

1. Copy the three test files (StudySpotTest.java, StudySpotListTest.java, ScheduleTest.java) into the top‐level directory.

2. Place junit-4.12.jar and hamcrest-core-1.3.jar alongside them.

3. Compile:
```
bash
# On macOS/Linux:
javac -cp .:junit-4.12.jar:hamcrest-core-1.3.jar *.java logic/*.java

# On Windows:
javac -cp .;junit-4.12.jar;hamcrest-core-1.3.jar *.java logic/*.java

```
4. Execute a test suite:
```
bash
java -cp .:junit-4.12.jar:hamcrest-core-1.3.jar org.junit.runner.JUnitCore StudySpotTest
```
*(Replace : with ; on Windows.)*

## 📜 Credits & Assets
- Map tiles and Google Maps assets are used under their respective terms.

- University of Calgary logo is a trademark of UCalgary.

