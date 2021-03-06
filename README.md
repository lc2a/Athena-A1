# [Athena-A1](https://www.asrockind.com/overview.tw.asp?Model=athena%20A1)  toolkits
<img width="=700" height="350" src="https://github.com/Asrockind/picture/blob/master/3.png"/> <br><br>
## Introduction

[ASRock Industrial’s](https://www.asrockind.com/) athena A1 Kit is an AI edge camera that supports Intel’s Movidus™ and [OpenVINO™ toolkits](https://software.intel.com/en-us/openvino-toolkit)(Open Visual Inferencing and Neural Network Optimization) for sophisticated video and image analysis applications. It is more flexible operation without chassis design for Maker and software developer to implement recognition training models.

The athena A1 AI edge camera delivers 2MP resolution (1080p) with 30 fps,and a H.264 codec combining high definition footage and powerful video stream analysis capabilities.

Support for AWS IoT Greengrass allows for the deployment of cloud enabled inference functionalities that create value-added solutions for use-cases in theft/crime prevention or consumer behavior analysis based on machine learning.

Athena have installed two Edge computing software SDK：[Intel OpenVINO Toolkit](https://software.intel.com/en-us/openvino-toolkit)(Open Visual Inferencing and Neural Network Optimization) and [AWS IoT Greengrass](https://aws.amazon.com/tw/greengrass/).Provide out-of-the-box AIoT development board,whithout tedious installation process. Plug-in has ready-made AIoT system. The system is x86 64bit CPU architecture and Ubuntu OS .  Through the applications with Athena A1 Kit maker can develope application easily. 

You can watch the [Video](https://youtu.be/u5mgDqoLPvg) to assemble the athena-A1.

Let me show athena A1 Kit spec： <br> 
 ![image](https://github.com/Asrockind/picture/blob/master/4.png)   ![image](https://github.com/Asrockind/picture/blob/master/athenaA1_2.png) <br> 

[From Asrockind](https://www.asrockind.com/overview.tw.asp?Model=athena%20A1)

## [Neural Compute Stick 2](https://software.intel.com/en-us/neural-compute-stick)
The Intel NCS 2(VPU) enables deep neural network testing, tuning and prototyping, so developers can go from prototyping into production leveraging a range of Intel vision accelerator form factors in real-world applications.<br>
Before use VPU to run demo. You must to run the batch file [vpu_init](https://github.com/Asrockind/Athena-A1/blob/master/vpu_init).
## Image File
The Athena-A1 system is default Ubuntu : 16.04 ,Openvino version :2019.1.144 . If you want to recover your system . You can download [image](https://drive.google.com/open?id=1trYd7I2uw6-VCvOnAYGnKYbe1JjqVDJD) to ghost to your athena-A1 . <br> 
Download the image file to your HDD or SSD. You have to use USB or other device to boot to Ubuntu. Open terminal and command as below:<br>  <br> 
Use root  <br>
`sudo su` <br><br>
Ghost to the Athena A1  <br>
`gzip -dc /imagefile_path/backupV008_customer.img.gz | dd of=/dev/mmcblk1` <br><br>
if it down you can see the information as below : <br>
`xxxxxx+0 record in`<br>
`xxxxxx+0 record out`<br>
` xxxxxxxxxx bytes (XXGB, XXGB) copied , xxxx s,21.0 MB/s` <br>
 it mean the ghost was finish and need to restart the system <br>
 
## Description

We provide some examples as below 
You can follow [demo](https://github.com/Asrockind/Athena-A1/blob/master/demo/demo) to command . <br>
### 1. Face detection 
This demo showcases Object Detection task applied for face recognition using sequence of neural networks. It detect age, gender, emation.<br><br>
<img width="=900" height="350" src="https://github.com/Asrockind/picture/blob/master/1.png"/> <br><br>

### 2. Pedestrian Tracker
This demo showcases Pedestrian Tracking scenario: it reads frames from an input video sequence, detects pedestrians in the frames, and builds trajectories of movement of the pedestrians in a frame-by-frame manner.  <br><br>
<img width="=700" height="250" src="https://github.com/Asrockind/picture/blob/master/pedestrian_tracker1.png"/> Before Inference <br>

After Inference as below 
<img width="=900" height="350" src="https://github.com/Asrockind/picture/blob/master/pedestrian_tracker5.png"/> <br><br>

### 3. Segmentation demo
This demo demonstrates how to run the Image Segmentation demo application, which does inference using image segmentation networks.<br><br>
Road-segmentation     : This is a segmentation network to classify each pixel into four classes: BG, road, curb, mark.<br>
Semantic-segmentation : This is a segmentation network to classify each pixel into 20 classes Road,sidewalk,building,wall,fence,pole,traffic light,traffic sign,vegetation,terrain,sky,person .... etc<br>

<br><br>
<img width="=1100" height="750" src="https://github.com/Asrockind/picture/blob/master/segmentation1.png"/> <br><br>

### 4. Security_barrier_camera_demo
This demo showcases Vehicle and License Plate Detection network followed by the Vehicle Attributes Recognition and License Plate Recognition networks applied on top of the detection results.
<br><br>
<img width="=800" height="450" src="https://github.com/Asrockind/picture/blob/master/security_berrier1.png"/> <br><br>
