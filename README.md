#**Real-Time Oil Spill Detection Using AIS and Satellite Data Integration**

An automated, intelligent framework for real-time maritime surveillance, combining deep learning models with vessel tracking data to detect and report oil spills.

🌟 **Project Overview**
This project presents a comprehensive solution to a critical environmental challenge: oil spills. Traditional detection methods are often slow and ineffective. Our system addresses these limitations by leveraging a powerful combination of technologies to provide real-time, accurate, and automated oil spill detection and identification of the responsible vessels.

We integrate two primary data sources:

**Automatic Identification System (AIS) Data:** Provides real-time vessel movement, speed, and location data. Anomalies in this data, like sudden speed drops or erratic navigation, can indicate potential spills.
**High-Resolution Satellite Imagery:** Specifically, we use images from Sentinel-1 (Synthetic Aperture Radar - SAR) and Sentinel-2 satellites, which are ideal for detecting oil slicks on the ocean surface, even in challenging weather conditions.

By fusing these data streams, our system not only detects spills but also correlates them with nearby vessel activities, a crucial step for environmental enforcement and accountability.

✨ **Key Features**

**Real-Time Anomaly Detection:** The system continuously monitors AIS data to flag suspicious vessel behavior that may lead to an oil spill.
**Hybrid AI Model:** A custom-trained deep learning model, combining the strengths of U-Net and DeepLabV3+ architectures, is used for precise image segmentation and spill detection.
  - U-Net excels at capturing fine-grained details and preserving spatial accuracy.
  - DeepLabV3+ is powerful for understanding broader context and minimizing false positives from visually similar phenomena like algal blooms or cloud shadows.
**Data Integration & Correlation:** AIS anomalies and satellite-detected spills are combined using geospatial mapping to pinpoint the likely source of a spill.
**Automated Alerts & Reporting:** The system sends immediate alerts to maritime and environmental authorities upon confirming a spill, including location, time, and potential vessel information.
**Scalable Architecture:** Built on a cloud-based infrastructure (Google Earth Engine), the system can scale to monitor wide oceanic regions efficiently and cost-effectively.

⚙️ **How It Works**
**AIS Data Ingestion:** The system continuously pulls real-time AIS data to track vessel movements.
**Anomaly Detection:** A module analyzes AIS data for irregular behavior (e.g., speed drops, sharp course changes) and flags suspicious vessels.
**Satellite Image Retrieval:** Upon detecting an anomaly, the system automatically fetches corresponding Sentinel-1/Sentinel-2 imagery from Google Earth Engine (GEE) for the flagged location.
**Deep Learning Analysis:** The hybrid U-Net + DeepLabV3+ model processes the satellite image. It segments the image pixel by pixel to identify and delineate oil spill areas with high accuracy, distinguishing them from other ocean features.
**Spill Confirmation & Correlation:** The system cross-references the image-based detection with the AIS data. If a spill is confirmed and a vessel is found to have been in the vicinity, an alert is triggered.



Alert & Visualization: Authorities receive a real-time alert via a web dashboard, which displays the spill location, affected area, and the suspected vessel's information on an interactive map.



🚀 Getting Started
Prerequisites
Python 3.10 or higher.

An NVIDIA GPU is recommended for faster model training and inference.


A Google Earth Engine (GEE) account and API credentials.

Installation
Clone the repository:

Bash

git clone https://github.com/uday1730/Real-Time-Oil-Spill-Detection-Using-AIS-And-Satellite-Data-Integration.git
cd Real-Time-Oil-Spill-Detection-Using-AIS-And-Satellite-Data-Integration
Install the required libraries:

Bash

pip install -r requirements.txt
Authenticate Google Earth Engine (GEE):

Bash

earthengine authenticate
Running the System
To run the main pipeline, execute the following command:

Bash

python main_code.py
This script will automatically load AIS data, detect anomalies, fetch satellite images, and run the deep learning models.

📂 Project Structure
main_code.py: The main script that orchestrates the entire pipeline.

unet_model.h5: The pre-trained U-Net model.

deeplabv3_model.h5: The pre-trained DeepLabV3+ model.

oil_spill_images.npy: Sample dataset of satellite images.

oil_spill_masks.npy: Ground truth masks for the images.

requirements.txt: List of all Python dependencies.

docs/: Project documentation and reports.

📈 Testing & Evaluation
The system was rigorously tested using various methodologies to ensure its reliability and accuracy. The confusion matrix below shows the performance of our hybrid model, achieving high accuracy in distinguishing oil spills from other classes.




Metric	Score
Overall Accuracy	~95%
False Positives	Minimized
False Negatives	Minimized

Export to Sheets
💡 Future Enhancements
Higher Resolution Imagery: Integrate with higher-resolution commercial satellites for even more precise detection.


Predictive Analytics: Incorporate meteorological and ocean current data to predict the trajectory and spread of detected spills.



User Interface: Develop an intuitive and robust web-based dashboard for authorities to monitor and manage incidents effectively.


Real-Time Streaming: Implement a more robust real-time data streaming and processing pipeline for immediate, continuous surveillance.
