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

## Built With

- ***[Python](https://www.python.org/)***

- ***[Yolov5](https://github.com/ultralytics/yolov5)***

- ***[EasyOCR](https://github.com/JaidedAI/EasyOCR)***

- ***[Raspberry Pi 4B](https://www.raspberrypi.com/products/raspberry-pi-4-model-b/)*** (optional)

- ***[Raspberry Pi Camerav2](https://www.raspberrypi.com/products/camera-module-v2/)*** (optional)

## Getting Started 

Before getting started, we need to have some data,software and access to some websites which is necessary for this project.

### Prerequisites

1. Bangladeshi Bangla License Plate Dataset
2. [Anconda](https://anaconda.org/anaconda/python) or [Pycharm](https://www.jetbrains.com/pycharm/download/) for model training 
3. Alernatively, we could also use [Google Colab](https://colab.research.google.com/) or similiar kind of cloud platform for model training 
4. A webcam if raspberry pi with its cmaera is not used 

### Steps

+ To train the model and run the whole project we will use [Anconda](https://anaconda.org/anaconda/python).First,we need to create a virtual environment in anaconda.To create a virtual environment,open anaconda promt from start menu and enter following command 
```
conda create -n {virtual environment name}
```
 Activate the virtual environment by issuing:
```
conda activate {virtual environment name}
```
+ Now make a directory in your preferable drive and create a folder where we will store all the necessery files.So,if needed, we change the directories in anaconda command prompt and create a folder and change directories to that folder.
```
mkdir <folder name>
cd <folder name>
```
+ Now we clone this repository to this folder by issuing:
```
git clone https://github.com/MahmudolHasan/Real-Time-Bangladeshi-License-Plate-Detection-And-Recognition
```
+ We have created  virtual environment and clone the repository.Now we need to prepare our data to train the model.We have already created a dataset of Bangladeshi license plate and it can be downloded from this link: [Bangla License Plate](https://www.kaggle.com/datasets/mahmudolhasantushar/bangla-license-plate "https://www.kaggle.com/datasets/mahmudolhasantushar/bangla-license-plate").In all, there are 295 images with annotations in the dataset.And they are splitted into three parts;train(70%), valid(20%) and test(10%).Now to preapre the dataset for training we will use [roboflow](https://app.roboflow.com/).They has a guidline on how to [prepare](https://blog.roboflow.com/getting-started-with-roboflow/) a dataset for taining. We will use anaconda to train  ourt yolov5 model.We could also use colab or kaggle to train the model.

+ We will install jupyter notebook to run allthe code.First we need to upgrade the pip to avoid any issue with dependencies by issuing:
```
pip3 install --upgrade pip
```
Afterward, install Jupyter Notebook by using:
```
pip3 install jupyter
```
To run the notebook:
```
jupyter notebook
```



