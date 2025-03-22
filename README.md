# Real-Time-Oil-Spill-Detection-Using-AIS-And-Satellite-Data-Integration

The primary objective of this project is to detect oil spills in the ocean using Sentinel-1 SAR (Synthetic Aperture Radar) satellite imagery. The project utilizes deep learning models, such as U-Net and DeepLabV3, for oil spill detection and incorporates vessel anomaly detection to identify regions of interest.  

Workflow Overview :

Model Training and Saving: Each deep learning model (U-Net and DeepLabV3) should be trained individually using the provided dataset.  

The trained models are saved in a designated folder for reuse. These models are later integrated and utilized in the Main_Code file for final predictions.  

Dataset Details :

Oil Spill Detection Dataset: Download both the train and test directories from the Kaggle dataset (https://www.kaggle.com/datasets/nabilsherif/oil-spill), which contains Sentinel-1 SAR imagery annotated for oil spills.  

AIS Vessel Data: Access vessel tracking data from Marine Cadastre (https://marinecadastre.gov/accessais/), which is essential for detecting ship anomalies and generating regions of interest for oil spill detection.  

Prerequisites :

Deep Learning Knowledge: Familiarity with models like U-Net and DeepLabV3 is required to train and fine-tune the models effectively.  

Python Programming: Proficiency in Python is essential for running and modifying the scripts.  

Required Libraries: Ensure all necessary dependencies are installed, including TensorFlow, Keras, and OpenCV. Use the requirements.txt file in the repository to set up the environment.  

Instructions :

1. Download the datasets mentioned above.  
2. Train each model using the respective script provided.  
3. Save the trained models in the models directory (or any specified path).  
4. Use the Main_Code file to combine oil spill detection and AIS-based anomaly detection for end-to-end processing.
