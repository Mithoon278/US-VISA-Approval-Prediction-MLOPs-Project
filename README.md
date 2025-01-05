
# US-VISA-Approval-Prediction-MLOPs-Project

The process of applying for a US visa is often lengthy, with numerous applications being rejected due to unmet criteria. To streamline this process and provide applicants with actionable insights, we have developed a machine learning-powered system that predicts the likelihood of visa approval. By analyzing the information provided by applicants, our solution offers a data-driven way to identify potential issues, enabling applicants to take corrective actions before submission.

## Project Overview:

This project aims to predict the outcome of US visa applications by developing a machine learning model. This model processes a series of input data to determine the likelihood of visa approval. We source our data from a comprehensive dataset available on Kaggle, which can be found at the following link: [EasyVisa Dataset](https://www.kaggle.com/datasets/moro23/easyvisa-dataset).

To refine our data and enhance the model's accuracy, we undertake Exploratory Data Analysis (EDA) and feature engineering. These critical steps are documented in our project notebooks, accessible via the following links:

* EDA Process: [EDA Notebook](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/notebook/1_EDA_US_visa.ipynb)
* Feature Engineering and Model Training: [Feature Engineering Notebook](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/notebook/2_Feature_Engineering_and_Model_Training.ipynb)

Our approach is not limited to a single machine learning algorithm; instead, we explore a variety of classification algorithms including Random Forest, Decision Tree, Gradient Boosting, Logistic Regression, K-Neighbors Classifier, XGBClassifier, and CatBoost Classifier. To optimize performance, we apply hyperparameter tuning to these models and select the most effective one based on predictive accuracy.

The project is structured in a modular code format, facilitating maintainability and scalability. Continuous Integration and Continuous Deployment (CI/CD) are implemented via GitHub Actions, ensuring automated testing and deployment. The final system is hosted on AWS, leveraging services such as S3 buckets, Elastic Container Registry (ECR), and EC2 instances to provide a robust and scalable solution.

## Project Workflow:

### Folder structure:
![alt text](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/flowcharts/folder_structure.png)

### Data Ingention flow : 

![alt text](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/flowcharts/Data%20Ingestion.png)

### Data Transformation flow : 

![alt text](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/flowcharts/Data%20Transformation.png)

### Data Validation flow:

![alt text](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/flowcharts/Data%20Validation.png)

### Model Trainer flow :

![alt text](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/flowcharts/Model%20Trainer.png)

### Model Evaluation flow :

![alt text](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/flowcharts/Model%20Evaluation.png)

### Model Pusher flow :

![alt text](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/flowcharts/Model%20Pusher.png)

## Demo :

![](https://github.com/Mithoon278/US-VISA-Approval-Prediction-MLOPs-Project/blob/main/flowcharts/Screen%20Recording%202025-01-05%20135306.gif)



## Tech stack: 

* **Python 🐍:** Our core programming language, chosen for its versatility and the vast ecosystem of data science libraries. 
    We adhere to a modular coding approach for better maintainability and readability.
* **Jupyter Notebook 📓:** Utilized for conducting Exploratory Data Analysis (EDA) and feature engineering, allowing us 
    to iteratively explore and visualize our data with ease.
* **VS Code 🛠️:** Our Integrated Development Environment (IDE) of choice, providing a powerful platform for code development 
    with extensive support for Python and data science workflows.
* **MongoDB 🍃:** This NoSQL document database stores and manages our visa application data. Its flexible schema and scalability 
    make it ideal for handling our large and complex datasets.
* **GitHub 🐱:** Serves as our version control system and the backbone for our Continuous Integration and Continuous Deployment 
    (CI/CD) workflows, ensuring our project remains collaborative and up-to-date.
* **FastAPI 🚀:** Chosen for its speed and ease of use, FastAPI helps us build our application's wireframe, enabling quick 
    and reliable interaction with our predictive model.
* **AWS ☁️:** Amazon Web Services provide the infrastructure for deploying our application/model. From compute power (EC2) to 
    storage (S3) and container management (ECR), AWS ensures our system is scalable, secure, and accessible.

## Git commands

```bash
git add .

git commit -m "Updated"

git push origin main
```


## How to run?

```bash
conda create -n visa python=3.8 -y
```

```bash
conda activate visa
```

```bash
pip install -r requirements.txt
```

## Workflow configuration:

1. constant
2. config_entity
3. artifact_entity
4. component
5. pipeline
6. app.py



### Export the  environment variable
```bash
export MONGODB_URL="mongodb+srv://<username>:<password>...."

export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>

export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>

```


# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 315865595366.dkr.ecr.us-east-1.amazonaws.com/visarepo

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
   - AWS_DEFAULT_REGION
   - ECR_REPO





## Feedback

If you have any feedback, please reach out to me at midhunbose2017@gmail.com

