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
        <li><a href="#Steps">Steps</a></li>
      </ul>
    </li>
    <li><a href="#Result">Result</a></li>
    <li><a href="#Contact">Contact</a></li>
    
  </ol>
</details>

## About The Project

This project aims to develop a system which can detect **Bangladeshi license plate (Bangla characters)** and recognizes the characters in the license plate.The licenese plate information will be saved in a xls file along with some other informations such as location,time,cropped picture of the license plate and an unique id for each deteced license plate. 

****Cite the dataset:**

**M. H. Tushar, M. T. Bhuiyan, M. S. Hossain, A. Tabassum and R. Khan, “Real Time Bangla License Plate Recognition with Deep Learning Techniques,” International Conference on Artificial Intelligence in Engineering and Technology (IICAIET), pp. 1-6, 2022.****

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

+ To train the model we will use google colab and run the whole project we will use anconda or terminal in case of raspberry pi.First,we need to create a virtual environment in anaconda.To create a virtual environment,open anaconda promt from start menu and enter following command 
```
conda create -n {virtual environment name}
```
 Activate the virtual environment by issuing:
```
conda activate {virtual environment name}
```
+ We have created  virtual environment.Now we need to prepare our data to train the model.We have already created a dataset of Bangladeshi license plate and it can be downloded from this link: [Bangla License Plate](https://www.kaggle.com/datasets/mahmudolhasantushar/bangla-license-plate "https://www.kaggle.com/datasets/mahmudolhasantushar/bangla-license-plate").In all, there are 295 images with annotations in the dataset.And they are splitted into three parts;train(70%), valid(20%) and test(10%).Now to preapre the dataset for training we will use [roboflow](https://app.roboflow.com/).They has a guidline on how to [prepare](https://blog.roboflow.com/getting-started-with-roboflow/) a dataset for taining. We will use colab to train our yolov5 model.We could also use anaconda or pycharm to train the model in local machine.

+  We trained the model in colab and downloaded the weights from colab.Two trained weights yolov5s & yolov5n will be included in this repository.

+ Now make a directory in your preferable drive and create a folder where we will store all the necessery files.So,if needed, we change the directories in anaconda command prompt and create a folder and change directories to that folder.
```
mkdir <folder name>
cd <folder name>
```
+ Now we clone yolov5 repository to this folder by issuing:
```
git clone https://github.com/ultralytics/yolov5 .
```
We need to delete the default detect.py that comes with yolov5 directory by using following command:
```
del detect.py
```
We will clone this repository for customized detect.py and trained weights.
```
git clone https://github.com/MahmudolHasan/Real-Time-Bangladeshi-License-Plate-Detection-And-Recognition .
```
We need to install and import python packages to run the detection by using:
```
pip install -r requirements.txt
```
we also need to install easyocr and xlswriter by issuing:
```
pip install easyocr==1.4.0
```
```
pip install xlsxwriter
```
```
pip install uuid
```
Now run following command to real time detect license plate:
```
python detect.py --weights yolov5s.pt --img 320 --conf 0.5 --source 0 --save-crop 
```
Note: use '--save-crop' to save the license plate information in an xls file.

## Result
#### Tested Cars pictures 

<p float="left">
  <img src="images/c1.jpg" alt="Vehicle 1" width="160" height ="150" />
  <img src="images/c2.jpg" alt="Vehicle 2" width="160" height ="150" /> 
  <img src="images/c3.jpg" alt="Vehicle 3" width="160" height ="150" />
  <img src="images/c4.jpg" alt="Vehicle 4" width="160" height ="150" />
  <img src="images/c5.jpg" alt="Vehicle 5" width="160" height ="150" >
</p>
    
#### The Output Result

<img width="800" src='images/result.png '>

## Contact
<a href="https://twitter.com/hasan_tusher" title="Follow@tusher_hasan" target="_blank" ><img src="https://img.icons8.com/fluency/48/000000/twitter.png" alt="twitter" style="width:40px;height:40px;"></a>    <a href="mailto:tusharhasan182@gmail.com" title="Send Email"><img src="https://img.icons8.com/doodle/48/000000/new-post.png" alt="Send Email" style="width:40px;height:40px;"></a>
