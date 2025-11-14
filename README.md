### Smart-Queue-Alert-System

AWS Rekognition + Google Colab | Cloud + AI Integration

A fully cloud-based system that detects and counts people in canteen queue images using AWS Rekognition, classifies queue levels, and generates smart alerts — all within the AWS Free Tier using Google Colab.

## 🚀 Project Overview

Campus canteens often experience unpredictable queues that waste student time.
This project solves that by using AI-powered person detection on uploaded queue images to estimate crowd size and display a real-time alert such as:

🍽️ “Low queue — go grab your food!”

🙂 “Moderate queue — just a little wait!”

😋 “Crowded — waiting makes the food tasty!”

🏗️ Architecture
User → Google Colab Notebook → AWS S3 Bucket → AWS Rekognition
                                         ↓
                              Annotated Results + Alerts


## AWS Components Used:

🗂️ Amazon S3 — Stores uploaded queue images and annotated outputs

🧠 AWS Rekognition — Detects and counts people in each image

🔐 AWS IAM — Provides secure API access via user credentials

☁️ Google Colab — Hosts notebook logic, visualization & evaluation

## ⚙️ Features

✅ Cloud-based, no physical sensors needed
✅ Real-time person detection using Rekognition
✅ Queue classification: Low, Moderate, Crowded
✅ Accuracy & precision evaluation using recent S3 uploads
✅ Annotated image visualization (bounding boxes)
✅ Scalable, lightweight, and fully Free Tier compatible

## 🧩 Technologies Used
Category	Tools / Services
Cloud Provider	AWS (S3, Rekognition, IAM)
Platform	Google Colab / Jupyter
Programming Language	Python 3
Libraries	boto3, opencv-python, matplotlib, pillow, numpy
Optional UI	Gradio / Flask
## 🧱 Setup Instructions
1️⃣ Clone this Repository
git clone https://github.com/<your-username>/smart-queue-alert.git
cd smart-queue-alert

 2️⃣ Open in Google Colab

Upload the notebook files or copy code blocks into a Colab notebook.

 3️⃣ Configure AWS Credentials

Create an IAM user with these permissions:

s3:PutObject
s3:GetObject
rekognition:DetectLabels
s3:ListBucket


Then enter your Access Key and Secret Key securely in Colab.

 4️⃣ Run Cells Sequentially

Upload an image of the canteen queue

Detect and count people using Rekognition

Annotate image and visualize results

View smart queue alerts and metrics

## 📊 Alert Logic
Detected People	Queue Status	Message
< 5	🟢 Low Queue	“Go grab your food!”
5–10	🟡 Moderate Queue	“Just a little wait 🙂”
> 10	🔴 Crowded	“Waiting makes the food tasty 😋”
🧮 Evaluation Metrics

Accuracy (%) = Correct classifications / Total

Precision (per class) = TP / (TP + FP)

Displays results for the last 2 uploaded images from your S3 bucket.

## 🧠 How It Works

Upload Image → via Colab file picker

Store Image in S3 → securely uploaded to your bucket

Analyze with Rekognition → detect “Person” labels

Generate Annotated Image → bounding boxes around detected people

Classify Queue Level → based on thresholds

Display Alert & Metrics → real-time feedback

## 📷 Sample Workflow Diagram
[User Uploads Image]
          |
          ▼
[Google Colab Notebook]
          |
          ▼
[S3 Bucket → AWS Rekognition]
          |
          ▼
[Person Detection + Count]
          |
          ▼
[Queue Level + Alert Generated]

## 🔐 Security Notes

IAM user has minimal privileges (S3 + Rekognition only).

Credentials are input securely and not stored in code.

Works entirely within AWS Free Tier limits.

## 📈 Future Enhancements

🧍‍♂️ Live camera feed analysis (via AWS Kinesis)

🌐 Web dashboard (S3 static site + Lambda API)

📩 SMS / Email queue alerts (AWS SNS)

🤖 Automatic trigger on new uploads (Lambda event)

## 🏁 Conclusion

The Smart Queue Alert System demonstrates how Cloud + AI integration can solve real-world campus challenges.
Using only serverless AWS tools, it delivers an intelligent, affordable, and scalable queue management system — all in the cloud.

## 👩‍💻 Author

Bharath Kumar Reddy
Cloud Computing Methodologies 
