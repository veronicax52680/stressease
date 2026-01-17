# StressEase 

## What Is It?
StressEase is a biomedical device that detects and calms a user’s stress response using collected data sorted using Python, machine learning, and AI-generated guidance. Stress is one of the most common mental health challenges today, and my goal was to create an accessible, and accurate Arduino-based system that helps people become aware of their daily stress patterns while actively seeking to improve it. 

## How It Works

### Step 1: Collecting the Data
The system starts off with collecting physiological data from two sensors connected to an **Arduino GIGA R1 WiFi board**. The **MAX30102** pulse oximetry heart rate monitor measures heart rate (BPM) and oxygen saturation (SpO2), while the **GSR sensor** measures skin conductivity in micro-Siemens (μS). 

These values are transmitted via Bluetooth to a Python program with **Bleak** and **ArduinoBLE** libraries. 

### Step 2: Using Machine Learning to Classify the Data 
Once received, the data is cleaned using **NumPy** and **Pandas**, removing missing or zero values. The cleaned data is then analyzed by a **Random Forest Classifier** machine learning model trained on stress and non-stress samples collected from volunteers*. Based on this, the model classifies whether the user is currently stressed or not.

<small> *For non-stress samples, I had the subject sit in a dark, quiet room for 10 minutes. To simulate a stress response, the subject was placed in the same room for the same amount of time but with visual and auditory stimuli from segments of horror movies or general “scary clips” found on YouTube. The stress data collection was completely optional, and some participants refused, leading to an unequal balance between stress/non-stress samples for the training data. That was mitigated by normalization. Through some experimentation with the sensors and preliminary data analysis, I discovered that when stressed, heart rate and skin conductance generally increases and SpO2 stays the same. </small>

### Step 3: AI Guidance Using ChatGPT
The result from the Random Forest Classifier is then sent to ChatGPT through the OpenAI API. If stress is detected, ChatGPT acts as a supportive “virtual psychologist”, offering a 100-200 word personalized message on mindfulness or relaxation techniques like breathing or taking a walk. If no stress is detected, it responds with positive reinforcement to encourage ongoing well-being. 