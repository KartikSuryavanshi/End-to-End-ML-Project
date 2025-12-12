📘 End-to-End Machine Learning Project: Student Marks Prediction

This project demonstrates an end-to-end machine learning pipeline that predicts student marks based on study hours.
It includes everything from data ingestion → model training → deployment → CI/CD on AWS using:

GitHub

AWS CodePipeline

AWS Elastic Beanstalk

🚀 Project Architecture
GitHub Repository → CodePipeline → Elastic Beanstalk → Live ML App

🧠 Tech Stack
Machine Learning

Python

Pandas, NumPy

Scikit-Learn

Pickle for model serialization

Backend

Flask

AWS Deployment

AWS CodePipeline (CI/CD)

AWS CodeBuild (optional)

AWS Elastic Beanstalk

AWS S3

🗂 Project Structure
ML-Projects/
├── data/
│   └── student.csv
├── src/
│   ├── components/
│   │   ├── data_ingestion.py
│   │   ├── data_transformation.py
│   │   ├── model_trainer.py
│   ├── pipeline/
│   │   ├── training_pipeline.py
│   │   └── prediction_pipeline.py
│   ├── utils.py
│   ├── exception.py
│   └── logger.py
├── templates/
│   └── index.html
├── application.py
├── requirements.txt
└── README.md

🤖 ML Pipeline Workflow
1️⃣ Data Ingestion

Loads dataset

Splits into train/test

Stores processed data

2️⃣ Data Transformation

Feature scaling

Missing value handling

Saves preprocessing pipeline

3️⃣ Model Training

Trains multiple ML models

Selects best model based on accuracy

Exports model as model.pkl

4️⃣ Prediction Pipeline

Loads trained model

Accepts input features

Produces predicted marks

🌐 Deployment Workflow (CI/CD on AWS)
1. Developer pushes code → GitHub

Triggers AWS CodePipeline automatically.

2. AWS CodePipeline

Pulls latest code

Builds package

Sends to Elastic Beanstalk

3. Elastic Beanstalk

Hosts ML web application

Serves prediction model

🛠 Run Locally
1. Clone repository
git clone https://github.com/KartikSuryavanshi/ML-Projects.git
cd ML-Projects

2. Create virtual environment
conda create -n mlproject python=3.8 -y
conda activate mlproject

3. Install dependencies
pip install -r requirements.txt

4. Start application
python application.py

🏗 Deploy on AWS Elastic Beanstalk
Initialize EB project
eb init

Create environment
eb create ml-env

Deploy
eb deploy

📬 API Endpoints
Method	Endpoint	Description
GET	/	Homepage
POST	/predict	Predicts student marks
🔧 Future Enhancements

Add Docker support

Hyperparameter tuning

Model monitoring

CloudWatch logging integration

👨‍💻 Author

Kartik Suryavanshi
GitHub: https://github.com/KartikSuryavanshi

⭐ If you find this project useful, please star the repository! ⭐
