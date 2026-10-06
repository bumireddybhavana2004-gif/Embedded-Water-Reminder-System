# Embedded-Water-Reminder-System
A smart embedded water-drinking reminder system designed to encourage regular hydration. The project uses a microcontroller-based approach with user input, display, RTC and reminder functionality to provide timely drinking alerts and demonstrate practical Embedded C and microcontroller interfacing.
# 💧 AquaGuardian – Smart Water Drinking Reminder System

AquaGuardian is an embedded-based **Smart Water Drinking Reminder System** designed to help users maintain regular hydration by providing timely reminders to drink water.

The system uses an **ARM7 microcontroller**, **Real-Time Clock (RTC)**, **16×2 LCD**, **4×4 matrix keypad**, **buzzer**, and **interrupt mechanism** to monitor time and generate scheduled drinking reminders.

---

## 📌 Project Overview

Maintaining proper hydration is important for overall health, but people often forget to drink water regularly due to busy schedules.

AquaGuardian addresses this problem by providing an automated reminder system. The user can configure the required reminder settings through the keypad, while the RTC keeps track of the current time.

When the configured reminder time is reached, the system activates the buzzer and displays a notification on the LCD, reminding the user to drink water.

---

## 🎯 Objectives

* Develop an automated water-drinking reminder system.
* Provide reminders at predefined time intervals.
* Maintain accurate time using an RTC.
* Provide a simple user interface using a keypad and LCD.
* Generate an audible alert using a buzzer.
* Use interrupts for efficient event handling.
* Implement the system using embedded C and ARM7 microcontroller peripherals.

---

## ✨ Features

* ⏰ Real-time clock-based operation
* 💧 Scheduled water-drinking reminders
* 📟 16×2 LCD display
* 🔢 4×4 matrix keypad for user input
* 🔔 Buzzer-based reminder notification
* ⚡ Interrupt-based event handling
* 🕐 Accurate time tracking using RTC
* 👤 Simple and user-friendly interface
* 🔧 Modular embedded C implementation

---

## 🧩 System Components

### Hardware Components

| Component            | Purpose                                      |
| -------------------- | -------------------------------------------- |
| ARM7 Microcontroller | Main controller of the system                |
| RTC                  | Maintains current date and time              |
| 16×2 LCD             | Displays time, status, and reminder messages |
| 4×4 Matrix Keypad    | Allows user interaction and configuration    |
| Buzzer               | Provides audible reminder alerts             |
| Push Button / Switch | Provides additional user control             |
| Power Supply         | Provides power to the system                 |

---

## 🖥️ Software Requirements

* Embedded C
* Keil µVision
* ARM7/LPC21xx development environment
* Suitable ARM7 compiler
* Flash/programming utility for the target microcontroller

---

## 🏗️ System Architecture

```text
                 ┌───────────────────┐
                 │   ARM7 MCU        │
                 │   / LPC21xx       │
                 └─────────┬─────────┘
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
     ┌─────────┐      ┌─────────┐      ┌─────────┐
     │   RTC   │      │   LCD   │      │ Keypad  │
     └─────────┘      └─────────┘      └─────────┘
          │                │                │
          │                │                │
          └────────────────┼────────────────┘
                           │
                           ▼
                      ┌─────────┐
                      │ Buzzer  │
                      └─────────┘
```

---

## ⚙️ Working Principle

The AquaGuardian system operates according to the following sequence:

### 1. System Initialization

When the system is powered ON, the microcontroller initializes:

* LCD
* RTC
* Keypad
* Buzzer
* Interrupt system

### 2. Time Monitoring

The RTC continuously maintains the current time.

The microcontroller periodically reads the RTC values and compares them with the configured reminder time.

### 3. User Configuration

The keypad allows the user to enter or configure the required settings.

The LCD provides visual feedback while the user interacts with the system.

### 4. Reminder Detection

The microcontroller continuously checks whether the current RTC time matches the configured reminder condition.

### 5. Reminder Alert

When the reminder condition is satisfied:

* The buzzer is activated.
* The LCD displays the appropriate reminder message.
* The user is alerted to drink water.

### 6. Continue Monitoring

After the reminder event is handled, the system returns to monitoring the RTC and waits for the next reminder.

---

## 🔄 Program Flow

```text
              START
                │
                ▼
       Initialize Peripherals
                │
                ▼
          Initialize RTC
                │
                ▼
         Initialize LCD
                │
                ▼
        Initialize Keypad
                │
                ▼
       Configure Interrupts
                │
                ▼
        Read Current Time
                │
                ▼
    Compare With Reminder Time
                │
          ┌─────┴─────┐
          │           │
         NO          YES
          │           │
          │           ▼
          │      Activate Buzzer
          │           │
          │           ▼
          │      Display Reminder
          │           │
          │           ▼
          └──────► Continue
                   Monitoring
```

---

## 📁 Project Structure

```text
Aquaguardian-Smart-Water-Drinking-Reminder-System/
│
├── main.c
├── aquaguardian.c
├── aquaguardian.h
│
├── rtc-1.c
├── rtc.h
│
├── lcd (1).c
├── lcd.h
│
├── kpm-1.c
├── kpm.h
│
├── interrupt-1.c
├── delay (1).c
├── types (1).h
│
└── README.md
```

---

## 🔧 Software Modules

### `main.c`

Contains the main program and controls the overall execution of the system.

### `aquaguardian.c`

Contains the main AquaGuardian application logic and reminder functionality.

### `aquaguardian.h`

Contains declarations and definitions associated with the AquaGuardian application.

### `rtc-1.c`

Handles RTC initialization and time/date-related operations.

### `rtc.h`

Contains RTC-related declarations and definitions.

### `lcd (1).c`

Provides functions for interfacing with the 16×2 LCD.

### `lcd.h`

Contains LCD function declarations and related definitions.

### `kpm-1.c`

Handles interfacing with the matrix keypad and reading user input.

### `kpm.h`

Contains keypad-related declarations and definitions.

### `interrupt-1.c`

Contains interrupt configuration and interrupt-handling functionality.

### `delay (1).c`

Provides delay functions required by different peripherals.

### `types (1).h`

Contains user-defined data types used throughout the project.

---

## 🧠 Key Embedded Concepts Used

This project demonstrates several important embedded-system concepts:

* ARM7 microcontroller programming
* Embedded C programming
* GPIO programming
* RTC interfacing
* LCD interfacing
* Matrix keypad interfacing
* Buzzer control
* Interrupt programming
* Peripheral initialization
* Modular programming
* Real-time event monitoring
* Hardware-software integration

---

## 🚀 Installation and Setup

### Step 1 – Clone the Repository

```bash
git clone https://github.com/<your-username>/Aquaguardian-Smart-Water-Drinking-Reminder-System.git
```

### Step 2 – Open the Project

Open the project in the appropriate ARM7 development environment such as **Keil µVision**.

### Step 3 – Add Source Files

Make sure all `.c` and `.h` files are included in the project.

### Step 4 – Configure the Target

Select the appropriate ARM7/LPC21xx target device and configure the required compiler and target settings.

### Step 5 – Build the Project

Compile the project and resolve any compiler or linker errors.

### Step 6 – Program the Microcontroller

Download the generated program into the target ARM7 development board using the appropriate programming/debugging interface.

---

## 🧪 Testing

The system can be tested using the following conditions:

| Test                       | Expected Result                     |
| -------------------------- | ----------------------------------- |
| Power ON                   | System initializes successfully     |
| RTC initialized            | Current time is displayed/available |
| Keypad input               | User input is detected              |
| Reminder condition reached | Buzzer is activated                 |
| Reminder triggered         | LCD displays notification           |
| Next reminder interval     | System continues monitoring         |

---

## 📊 Advantages

* Simple and easy to operate
* Provides automatic hydration reminders
* Uses accurate RTC-based timing
* Low-cost embedded implementation
* Provides both visual and audible notifications
* Demonstrates practical embedded-system concepts
* Modular software structure makes development easier

---

## ⚠️ Limitations

* Reminder functionality depends on the configured time settings.
* The system requires a continuous power supply.
* The basic system does not automatically measure the amount of water consumed.
* It does not automatically determine an individual's ideal daily water requirement.
* Hardware configuration may need to be modified for different ARM7 boards.

---

## 🔮 Future Enhancements

The system can be extended with additional features such as:

* 📱 Mobile application connectivity
* 📡 Bluetooth/Wi-Fi connectivity
* 📊 Daily and weekly hydration statistics
* 💧 Water-level or flow sensing
* 🔔 Customizable reminder intervals
* 🔋 Battery-powered operation
* ☁️ Cloud-based data storage
* 📈 Hydration monitoring dashboard
* 👤 Personalized reminder schedules
* 🔊 Voice-based reminders

---

## 🎓 Applications

AquaGuardian can be useful for:

* Students
* Office workers
* Elderly people
* People with busy schedules
* Home users
* Workplace environments
* General hydration-awareness applications

---

## 🛠️ Technologies Used

**Programming Language**

* Embedded C

**Microcontroller**

* ARM7 / LPC21xx

**Development Environment**

* Keil µVision

**Interfaces**

* GPIO
* RTC
* LCD
* Matrix Keypad
* Interrupts

---

## 📚 Learning Outcomes

Through this project, the following practical skills can be developed:

* Understanding ARM7 architecture and peripherals
* Writing embedded C programs
* Interfacing external hardware with a microcontroller
* Working with RTC-based applications
* Implementing LCD and keypad drivers
* Understanding interrupt-driven programming
* Designing modular embedded software
* Debugging hardware and software integration issues

---

## 👩‍💻 Author

**Your Name**

Embedded Systems | ARM7 | Embedded C

GitHub: `https://github.com/<your-username>`

---

## 📜 License

This project is intended for educational and learning purposes.

You may modify and extend the project for academic and personal learning applications.

---

## ⭐ Acknowledgement

This project was developed as an embedded-systems project to demonstrate the integration of a microcontroller with RTC, LCD, keypad, buzzer, and interrupt-based peripherals to create a practical real-time reminder system.

---

## ⭐ If You Find This Project Useful

Consider giving the repository a ⭐ on GitHub and feel free to improve the project with additional embedded features.
