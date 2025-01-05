# Voice Prescription Web App

**Voice Prescription Web App** is an AI-enabled medical application that simplifies the process of online consultations and prescription generation for both patients and doctors. Leveraging **machine learning** and **NLP**, the app extracts relevant information from patient queries and allows doctors to generate prescriptions through voice input, which are processed and emailed as PDFs to the patients.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [System Workflow](#system-workflow)
- [Installation](#installation)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Future Enhancements](#future-enhancements)

---

## Overview

The **Voice Prescription Web App** provides a platform for seamless interaction between patients and doctors:
- Patients can submit symptoms and queries through voice input.
- The app processes and extracts key details such as **name, age, symptoms, and disease** using **NLP**.
- Doctors can generate prescriptions via voice input, which are transcribed and sent as a **PDF** to patients.

---

# Features

### For Patients:
- **Voice Input**: Submit symptoms and queries via speech, with real-time transcription.
- **Doctor Recommendations**: Suggests doctors based on symptoms using a **machine learning model**.
- **Prescription PDF**: Receive detailed prescriptions (disease, symptoms, medicines, advice) via email.
- **Chatbot Assistance**: AI-powered chatbot to assist with basic symptom queries and guide users through the platform.

### For Doctors:
- **Voice-Driven Prescription**: Generate prescriptions using voice, processed into structured data.
- **Automatic PDF Generation**: Convert transcribed prescriptions into PDF format for patient records.
- **Patient Query Management**: Access and manage patient-submitted queries.

### General Features:
- **NLP-Enabled Processing**: Extract structured data (e.g., name, symptoms) from unstructured input.
- **Multi-Language Support**: Process and understand voice input and NLP in multiple languages.
- **Email Notifications**: Send prescriptions directly to patients via email.
- **Data Storage**: Efficient storage and retrieval of patient and prescription data.

---

## Technologies Used

### Backend:
- **Flask**: Lightweight backend framework for building APIs.
- **NLP with SpaCy**: For entity extraction and natural language understanding.
- **Chrome Speech-to-Text API**: For real-time voice-to-text conversion.
- **SMTP Library**: For sending email notifications to patients.

### Machine Learning:
- **Scikit-Learn**: For training a machine learning model to recommend doctors based on symptoms.

### Chatbot:
- **Dialogflow**: AI-powered conversational chatbot for assisting users with queries.

### Multi-Language Support:
- **Google Translate API**: Handles language translation for NLP and chatbot functionalities.

### Database:
- **SQLite**: Lightweight database for storing patient queries, doctor information, and prescriptions.

---

## System Workflow

1. **Patient Portal**:
   - Patients submit voice queries in their preferred language.
   - NLP processes and extracts details like **name**, **age**, and **symptoms**.
   - Doctor recommendations are made based on the symptoms.

2. **Doctor Portal**:
   - Doctors receive patient details and submit prescriptions via voice input.
   - NLP structures the transcribed data into disease, symptoms, medicines, and advice.

3. **Chatbot Assistance**:
   - An AI chatbot provides guidance to patients and answers common queries.
   - Supports multi-language interactions for a global user base.

4. **Prescription Delivery**:
   - A PDF of the prescription is generated and sent to the patient's email.

---

## Installation

### Prerequisites:
- Python 3.7+
- Virtual environment (optional but recommended)
- Google Chrome (for Chrome Speech-to-Text API)
- Google Cloud Project for Dialogflow and Translate API

### Setup:
1. Clone the repository:
   ```
   git clone https://github.com/your-username/voice-prescription-web-app.git
   cd voice-prescription-web-app
   ```

2. Create and activate a virtual environment:
```
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```
pip install -r requirements.txt
```

4. Set up the database:
```
python database.py
```

5. Run the application:
```
python app.py
```
---

## Usage

### Patient Portal:
- Open the patient portal.
- Submit your symptoms and details using the voice input field.
- Receive a doctor recommendation based on your symptoms.

### Doctor Portal:
- Log in to the doctor portal.
- Review patient queries and submit prescriptions via voice.
- The system will email the prescription to the patient as a PDF.

---

## API Endpoints

### Patient:
- **POST** /api/patient/query: Submit patient symptoms and details.
- **GET** /api/patient/recommend-doctors: Get doctor recommendations based on symptoms.

### Doctor:
- **POST** /api/doctor/prescription: Submit a prescription for a patient.
- **GET** /api/doctor/queries: Retrieve pending patient queries.

### General:
- **POST** /api/auth/login: Login for doctors and admin.
- **GET** /api/data/export: Export prescription data in structured formats.

---

## Future Enhancements
- Integration with EHR: Enable integration with electronic health records for seamless data sharing.
- Advanced Analytics: Provide detailed analytics for doctors and patients.

---

## Happy Prescribing! 🩺✨
