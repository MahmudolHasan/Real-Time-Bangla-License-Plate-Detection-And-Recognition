<div id='top'></div>
<br />
<h1 align="center">
     Real-Time-Bangladeshi-License-Plate-Detection-And-Recognition
</h1>


<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
      <ul>
        <li><a href="#built-with">Built With</a></li>
      </ul>
    </li>
    <li>
      <a href="#getting-started">Getting Started</a>
      <ul>
        <li><a href="#prerequisites">Prerequisites</a></li>
        <li><a href="#installation">Installation</a></li>
      </ul>
    </li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

## About The Project

This project aims to develop a system which can detect **Bangladeshi license plate (Bangla characters)** and recognizes the characters in the license plate.The licenese plate information will be saved in a xls file along with some other informations such as location,time,cropped picture of the license plate and an unique id for each deteced license plate. 

##Built With

-***[Python](https://www.python.org/)***
-***[Raspberry Pi 4B](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/)***
-***[Raspberry Pi Camerav2](https://www.raspberrypi.com/products/camera-module-v2/)***



For the detection  we used the ***[Yolov5](https://github.com/ultralytics/yolov5)*** model and we also utilized the ***[EasyOCR](https://github.com/JaidedAI/EasyOCR "Ready-to-use OCR with 80+ supported languages and all popular writing scripts including: Latin, Chinese, Arabic, Devanagari, Cyrillic, etc.")*** to extract the character from the license plate.The Dataset was initially collected from a kaggle account to train the model. Later we created our own dataset and merged the two datasets.The dataset pre-processing and augmentation was done in roboflow.The dataset contains about 2.3K pictures of Bnagla License Plate.As the project was implemented in Raspberry Pi 4B, we choose the yolov5s for better and faster performance.
