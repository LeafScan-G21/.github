<!-- Banner -->
<p align="center">
  <img src="https://img.shields.io/badge/LeafScan-%2328a745.svg?style=for-the-badge&logo=leaflet&logoColor=white" alt="LeafScan Badge" />
</p>

<h1 align="center" style="color:#28a745;">🌿 LeafScan: Intelligent Plant Disease Detection & Care Advisory System</h1>

<p align="center">
  <em>AI-driven precision agriculture for a greener tomorrow 🌱</em>
</p>

<p align="center">
  <img src="https://github.com/your-org-name/LeafScan/assets/green-leaf-animation.gif" width="70%" alt="Animated Leaf Banner">
</p>

---

## 🧩 About the Project

**LeafScan** is an AI-powered plant disease detection and care advisory system built to help farmers, gardeners, and plant enthusiasts identify diseases from leaf images and receive personalized care instructions.  
Using a combination of **deep learning**, **cloud integration**, and **real-time weather intelligence**, LeafScan bridges the gap between technology and sustainable agriculture.

> 🌱 “We built LeafScan to empower the green world — one plant at a time.”

---

## 🎯 Why We Built This

Farmers often face difficulty identifying plant diseases early enough to act effectively. Manual diagnosis can be time-consuming, inaccurate, or dependent on expert availability.  
Our system was designed to solve this — by making **AI-based plant health monitoring** accessible, intelligent, and practical.

- 🌾 Early and accurate disease detection  
- ☁️ Cloud storage for historical records  
- ☀️ Weather-based care recommendations  
- 💬 Automated email notifications with results  
- 📈 Data-driven insights for sustainable agriculture  

We used the **PlantVillage dataset** to train our model, ensuring high accuracy and robustness across various plant species and diseases.

---

## 🧠 System Overview

### 🔍 How It Works
1. The user uploads an image of a diseased leaf.  
2. The image is preprocessed (cropped and resized).  
3. The system predicts the disease using our ML model.  
4. Weather data (via OpenWeather API) is fetched based on user’s location.  
5. Care advice is tailored dynamically considering weather and disease.  
6. The final report is emailed to the user and stored in the history service.  

---

## 🏗️ System Architecture

```mermaid
graph TD
A[📱 User Interface (React)] -->|Upload Image| B[(FastAPI Backend)]
B --> C[🧠 ML Prediction Service (CNN Model - PlantVillage)]
B --> D[(☁️ Cloudinary Storage)]
B --> E[(🌦️ Weather API Integration)]
B --> F[(📨 Email Notification Service)]
B --> G[(📜 History Service - MongoDB)]
C --> H[(🎯 Result Aggregation)]
E --> H
H -->|JSON Response| A
