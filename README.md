## Smart Queue Alert System

A cloud-powered crowd detection tool using AWS Rekognition.

## 📌 Project Description

This project automatically detects and counts the number of people in canteen queue images using AWS Rekognition. The system runs entirely through Google Colab, where users upload images that are stored in Amazon S3, analyzed by Rekognition, and returned with annotated bounding boxes and a queue alert message.

The project helps estimate queue length without any physical sensors, making it affordable, serverless, and easily scalable within the AWS Free Tier.

## ⚙️ Key Features

Automated person detection in uploaded images

Accurate crowd counting using Rekognition

Smart queue alerts: Low / Moderate / Crowded

Annotated output images generated with bounding boxes

Lightweight workflow implemented in Google Colab

Optional accuracy & precision evaluation using latest S3 uploads

##  Architecture
User → Google Colab Notebook → AWS S3 Bucket → AWS Rekognition
                                   ↓
                         Annotated Image + Queue Alert

##  Queue Alert Logic
People Detected	Queue Status	Message
< 5	 -- Low	“Go grab your food 🍽️”
5–10 --	Moderate	“Just a little wait 🙂”
> 10 --	Crowded	“Waiting makes the food tasty 😋”

##  Technologies Used

Python, Google Colab

AWS Rekognition, Amazon S3, AWS IAM , AWS CLI

Libraries: boto3, pillow, numpy, opencv-python, matplotlib

##  Workflow Summary

User uploads an image in Google Colab

Image is uploaded to S3

Rekognition analyzes and detects people

Results are returned to Colab
