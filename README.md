# 🧤 Smart Glove - Sign Language Recognition System

Welcome to the **Smart Glove** project! This IoT-based system is designed to translate sign language into text in real-time. 

Our primary mission is to break down communication barriers. This application exists to help people who do not know sign language easily understand and communicate with individuals who have speech or hearing impairments, fostering a more inclusive environment.

## 🏗️ Project Architecture

To ensure scalability and performance, the system is built using a microservices architecture. The source code is divided into three separate repositories:

* 📱 **[Mobile Application (Android)](https://github.com/LevapsP/SmartGlove-Mobile):** The client-side application. It serves as the user interface to connect the glove hardware, manage AI models, and display the translated gestures.
* 🧠 **[Machine Learning Service (Python)](https://github.com/DmytroKyryliuk2023/smart-glove-ml):** The AI engine of the project. It receives raw coordinate data from the backend via RabbitMQ, processes it through a neural network, and returns the recognized gesture.
* ⚙️ **[Core Backend Server (Java)](https://github.com/Rozzzchepiy/smartglove-core-backend):** Built with Java 21 and Spring Boot. It acts as the central hub, managing user authentication, routing sensor data, and storing AI models using MongoDB and MinIO.


## 🚀 How to Use the Application

To start using the Smart Glove system, follow these steps:

**1. Download and Install the App**
Download the `SmartGlove.apk` file directly from this repository and install it on your Android device.

**2. Hardware Setup (Bluetooth)**
Put the physical Smart Glove on your hand and turn it on. Open your phone's **Bluetooth** settings and pair it with the glove so it can start transmitting real-time sensor data to the application.

**3. Application Modes**
Launch the app. Inside, you will find two main tabs depending on what you want to achieve:

* 🎯 **Predict Mode (Translation):** This is the main mode for everyday communication. Simply select an AI model and start making signs with the glove. The app will capture your hand movements, send the coordinates to the server, and instantly display the recognized letters or words on your screen.
    
* 🏋️ **Train Mode (Learning):** Use this mode to teach the system new gestures or improve its accuracy. You can select a specific letter/word and perform the gesture multiple times. The app will record this data to train a personalized AI model tailored to your specific hand movements.
