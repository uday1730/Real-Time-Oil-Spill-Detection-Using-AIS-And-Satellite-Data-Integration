# Real-Time Oil Spill Detection Using AIS and Satellite Data Integration

[cite\_start]An automated, intelligent framework for real-time maritime surveillance, combining deep learning models with vessel tracking data to detect and report oil spills[cite: 1, 153].

-----

## 🌟 Project Overview

[cite\_start]This project presents a comprehensive solution to a critical environmental challenge: oil spills[cite: 152, 153]. [cite\_start]Traditional detection methods are often slow and ineffective[cite: 181]. [cite\_start]Our system addresses these limitations by leveraging a powerful combination of technologies to provide **real-time, accurate, and automated oil spill detection** and identification of the responsible vessels[cite: 158, 300].

We integrate two primary data sources:

  * [cite\_start]**Automatic Identification System (AIS) Data:** Provides real-time vessel movement, speed, and location data[cite: 154, 183]. [cite\_start]Anomalies in this data, like sudden speed drops or erratic navigation, can indicate potential spills[cite: 156].
  * [cite\_start]**High-Resolution Satellite Imagery:** We use images from **Sentinel-1 (Synthetic Aperture Radar - SAR)** and **Sentinel-2** satellites, which are ideal for detecting oil slicks on the ocean surface, even in challenging weather conditions[cite: 154, 183, 306, 307].

[cite\_start]By fusing these data streams, our system not only detects spills but also correlates them with nearby vessel activities, a crucial step for environmental enforcement and accountability[cite: 158, 160, 313].

-----

## ✨ Key Features

  * [cite\_start]**Real-Time Anomaly Detection:** The system continuously monitors AIS data to flag suspicious vessel behavior that may lead to an oil spill[cite: 156, 303, 304].
  * [cite\_start]**Hybrid AI Model:** A custom-trained deep learning model, combining the strengths of **U-Net** and **DeepLabV3+** architectures, is used for precise image segmentation and spill detection[cite: 185, 246].
      * [cite\_start]U-Net is proficient in capturing fine-grained edges and preserving spatial integrity[cite: 248].
      * [cite\_start]DeepLabV3+ excels at understanding the broader context and reducing classification errors[cite: 248].
  * [cite\_start]**Data Integration & Correlation:** The integration of AIS and satellite data significantly improves the accuracy, speed, and reliability of oil spill detection[cite: 158].
  * [cite\_start]**Automated Alerts & Reporting:** The system provides real-time alerts and generates visual reports with vessel identity, location coordinates, and time[cite: 160, 314, 315, 317].
  * [cite\_start]**Scalable Architecture:** The scalable nature of the system allows for integration with meteorological data and supports large-scale deployment by using cloud platforms like Google Earth Engine[cite: 162, 332].

-----

## ⚙️ How It Works

  * [cite\_start]**AIS Data Ingestion:** The system monitors real-time AIS data to track vessel movements[cite: 154].
  * [cite\_start]**Anomaly Detection:** Machine learning algorithms are applied to detect abnormal vessel behavior, such as abrupt speed reductions or erratic navigation[cite: 156].
  * [cite\_start]**Satellite Image Retrieval:** Upon detecting an anomaly, the system fetches corresponding Sentinel-1/Sentinel-2 imagery from Google Earth Engine (GEE)[cite: 306].
  * [cite\_start]**Deep Learning Analysis:** A custom-trained hybrid deep learning model processes the satellite image using advanced image analysis techniques, including segmentation and classification, to pinpoint suspicious surface patterns[cite: 157, 309].
  * [cite\_start]**Spill Confirmation & Correlation:** The system cross-references the image-based detection with the AIS data[cite: 160]. [cite\_start]If a spill is confirmed and a vessel is found to have been in the vicinity, an alert is triggered[cite: 160, 315].
  * [cite\_start]**Alert & Visualization:** The system sends immediate alerts and generates reports that can be accessed through a web dashboard, which displays the spill location, affected area, and the suspected vessel's information on an interactive map[cite: 318, 317].

-----

## 🚀 Getting Started

### Prerequisites

  * [cite\_start]Python 3.10 or higher[cite: 563].
  * [cite\_start]An NVIDIA GPU is recommended for faster model training and inference[cite: 557, 2341].
  * [cite\_start]A Google Earth Engine (GEE) account and API credentials[cite: 2345].

### Installation

1.  Clone the repository:
    ```bash
    git clone https://github.com/uday1730/Real-Time-Oil-Spill-Detection-Using-AIS-And-Satellite-Data-Integration.git
    cd Real-Time-Oil-Spill-Detection-Using-AIS-And-Satellite-Data-Integration
    ```
2.  Install the required libraries:
    ```bash
    pip install -r requirements.txt
    ```
3.  Authenticate Google Earth Engine (GEE):
    ```bash
    earthengine authenticate
    ```

### Running the System

To run the main pipeline, execute the following command:

```bash
python main_code.py
```

This script will automatically load AIS data, detect anomalies, fetch satellite images, and run the deep learning models.

-----

## 📂 Project Structure

  * `main_code.py`: The main script that orchestrates the entire pipeline.
  * `unet_model.h5`: The pre-trained U-Net model.
  * `deeplabv3_model.h5`: The pre-trained DeepLabV3+ model.
  * `oil_spill_images.npy`: Sample dataset of satellite images.
  * `oil_spill_masks.npy`: Ground truth masks for the images.
  * `requirements.txt`: List of all Python dependencies.
  * `docs/`: Project documentation and reports.

-----

## 📈 Testing & Evaluation

[cite\_start]The system was rigorously tested using various methodologies to ensure its reliability and accuracy[cite: 1646]. [cite\_start]The confusion matrix shows the performance of our hybrid model, achieving high accuracy in distinguishing oil spills from other classes[cite: 2179]. [cite\_start]When the model was tested, it achieved 95 percent accuracy overall[cite: 2179]. [cite\_start]False positives and false negatives were minimized to improve reliability[cite: 1649].

| Metric | Score |
| :--- | :--- |
| Overall Accuracy | [cite\_start]\~95% [cite: 2179] |
| False Positives | [cite\_start]Minimized [cite: 1649, 2135, 2323] |
| False Negatives | [cite\_start]Minimized [cite: 1650] |

-----

## 💡 Future Enhancements

  * [cite\_start]**Enhanced Spill Detection Accuracy:** Future work will focus on utilizing higher-resolution satellite imagery for better segmentation [cite: 2380] [cite\_start]and expanding training datasets to improve model performance in diverse conditions[cite: 2381].
  * [cite\_start]**Real-Time Processing & Alerts:** Future enhancements will include implementing real-time monitoring for immediate spill detection [cite: 2383] [cite\_start]and developing an automated alert system to notify authorities instantly[cite: 2384].
  * [cite\_start]**Improved AIS Correlation and Vessel Tracking:** Future improvements will focus on addressing gaps in AIS data by integrating additional vessel tracking sources [cite: 2386] [cite\_start]and optimizing anomaly detection algorithms to reduce false positives[cite: 2387].
  * [cite\_start]**Deployment & Scalability:** Future work will involve developing a user-friendly interface for environmental agencies [cite: 2389] [cite\_start]and implementing cloud-based deployment for large-scale monitoring[cite: 2389].
