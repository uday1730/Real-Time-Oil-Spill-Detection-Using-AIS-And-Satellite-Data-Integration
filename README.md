# Real-Time Oil Spill Detection Using AIS and Satellite Data Integration

An automated, intelligent framework for real-time maritime surveillance, combining deep learning models with vessel tracking data to detect and report oil spills.

## 🌟 Project Overview

This project presents a comprehensive solution to a critical environmental challenge: oil spills. Traditional detection methods are often slow and ineffective. Our system addresses these limitations by leveraging a powerful combination of technologies to provide **real-time, accurate, and automated oil spill detection** and identification of the responsible vessels.

We integrate two primary data sources:

  * **Automatic Identification System (AIS) Data:** Provides real-time vessel movement, speed, and location data. Anomalies in this data, like sudden speed drops or erratic navigation, can indicate potential spills.
  * **High-Resolution Satellite Imagery:** We use images from **Sentinel-1 (Synthetic Aperture Radar - SAR)** and **Sentinel-2** satellites, which are ideal for detecting oil slicks on the ocean surface, even in challenging weather conditions.

By fusing these data streams, our system not only detects spills but also correlates them with nearby vessel activities, a crucial step for environmental enforcement and accountability.

## ✨ Key Features

* **Real-Time Anomaly Detection:** The system continuously monitors AIS data to flag suspicious vessel behavior that may lead to an oil spill.  
* **Hybrid AI Model:** A custom-trained deep learning model, combining the strengths of **U-Net** and **DeepLabV3+** architectures, is used for precise image segmentation and spill detection.  
  * U-Net is proficient in capturing fine-grained edges and preserving spatial integrity.  
  * DeepLabV3+ excels at understanding the broader context and reducing classification errors.  
* **Data Integration & Correlation:** The integration of AIS and satellite data significantly improves the accuracy, speed, and reliability of oil spill detection.  
* **Automated Alerts & Reporting:** The system provides real-time alerts and generates visual reports with vessel identity, location coordinates, and time.  
* **Scalable Architecture:** The scalable nature of the system allows for integration with meteorological data and supports large-scale deployment by using cloud platforms like Google Earth Engine.  


## ⚙️ How It Works

* **AIS Data Ingestion:** The system monitors real-time AIS data to track vessel movements.  
* **Anomaly Detection:** Machine learning algorithms are applied to detect abnormal vessel behavior, such as abrupt speed reductions or erratic navigation.  
* **Satellite Image Retrieval:** Upon detecting an anomaly, the system fetches corresponding Sentinel-1/Sentinel-2 imagery from Google Earth Engine (GEE).  
* **Deep Learning Analysis:** A custom-trained hybrid deep learning model processes the satellite image using advanced image analysis techniques, including segmentation and classification, to pinpoint suspicious surface patterns.  
* **Spill Confirmation & Correlation:** The system cross-references the image-based detection with AIS data. If a spill is confirmed and a vessel is found to have been in the vicinity, an alert is triggered.  
* **Alert & Visualization:** The system sends immediate alerts and generates reports that can be accessed through a web dashboard, which displays the spill location, affected area, and the suspected vessel's information on an interactive map.  

## 🚀 Getting Started

### Prerequisites

  * Python 3.10 or higher.
  * An NVIDIA GPU is recommended for faster model training and inference.
  * A Google Earth Engine (GEE) account and API credentials.

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

## 📂 Project Structure

The repository is organized to facilitate easy navigation and understanding of the project's components.

  * `docs/`: Contains project documentation, reports, and other relevant academic materials.
  * `website/`: Holds the files for the web-based user interface, including HTML, CSS, and JavaScript.
  * `DeeplabV3.ipynb`: Jupyter Notebook for the DeepLabV3+ model implementation and experimentation.
  * `U_Net.ipynb`: Jupyter Notebook for the U-Net model implementation and experimentation.
  * `Hybrid.ipynb`: Jupyter Notebook detailing the hybrid model that combines UNET and DeepLabV3+ for enhanced detection.
  * `FinalOutput.ipynb`: A script for running the complete detection pipeline and generating the final output.
  * `CSV_Filter.csv`: Raw AIS data file used for initial filtering.
  * `filtered_ais_data.csv`: Preprocessed AIS data used for anomaly detection.
  * `requirements.txt`: A list of all Python dependencies required to run the project.

## 📈 Testing & Evaluation

The system was rigorously tested using various methodologies to ensure its reliability and accuracy. The confusion matrix demonstrated the hybrid model’s strong performance in distinguishing oil spills from other classes. When tested, the model achieved 95% overall accuracy. False positives and false negatives were minimized to enhance detection reliability.

| Metric           | Score     |
| :--------------- | :-------- |
| Overall Accuracy | ~95%      |
| False Positives  | Minimized |
| False Negatives  | Minimized |

## 💡 Future Enhancements

* **Enhanced Spill Detection Accuracy:** Future work will focus on utilizing higher-resolution satellite imagery for better segmentation and expanding training datasets to improve model performance in diverse conditions.  
* **Real-Time Processing & Alerts:** Future enhancements will include implementing real-time monitoring for immediate spill detection and developing an automated alert system to notify authorities instantly.  
* **Improved AIS Correlation and Vessel Tracking:** Future improvements will address gaps in AIS data by integrating additional vessel tracking sources and optimizing anomaly detection algorithms to reduce false positives.  
* **Deployment & Scalability:** Future work will involve developing a user-friendly interface for environmental agencies and implementing cloud-based deployment for large-scale monitoring.  
