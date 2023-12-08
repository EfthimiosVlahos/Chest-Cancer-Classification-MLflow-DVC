# Chest-Cancer-Classification-MLflow-DVC

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [MLflow and MLOps Best Practices](#mlflow-and-mlops-best-practices)
4. [Deployment and Technologies](#deployment-and-technologies)
5. [How to Run](#how-to-run)
6. [License](#license)
7. [Contact](#contact)

## Project Overview
This project is focused on leveraging advanced machine learning techniques for the accurate classification of chest cancer from medical imaging data. With the primary goal of enhancing the accuracy and efficiency of cancer diagnosis, this project employs sophisticated algorithms and neural network architectures tailored for image recognition and analysis.

Key aspects of the project include:
- **Data Handling:** Utilizing a comprehensive dataset of chest medical images, which includes a variety of cancerous and non-cancerous cases. The dataset is managed with Data Version Control (DVC), ensuring efficient handling of large datasets and reproducibility of experiments.
- **Model Development and Training:** Development of deep learning models, potentially employing Convolutional Neural Networks (CNNs), to classify images with high accuracy. Regular model training iterations are conducted to optimize accuracy and minimize false positives and negatives.
- **MLflow for Model Management:** MLflow is used extensively for tracking experiments, managing the machine learning lifecycle, including model versioning, parameter tuning, and result logging. This facilitates a systematic approach to model improvement and collaboration among team members.
- **Evaluation and Validation:** Rigorous evaluation protocols are in place to assess the model's performance, including sensitivity, specificity, and predictive values. Validation strategies include cross-validation and testing on a separate validation set to ensure generalizability of the model.
- **MLOps Best Practices:** Implementing MLOps best practices to streamline the workflow from data preprocessing to model deployment. This includes automation of various stages and ensuring model quality before deployment.
- **Deployment Strategy:** Details on how the model is deployed into a production environment. This could include integration with medical image analysis systems or deployment in a cloud-based setting for accessibility.
- **Ethical Considerations and Compliance:** Addressing ethical considerations and compliance with medical and data privacy regulations, ensuring that the model's deployment aligns with healthcare standards and patient privacy laws.

The project is a showcase of the practical application of machine learning in healthcare and aims to contribute towards advancements in medical diagnostics. By combining cutting-edge ML techniques with robust data and model management tools like MLflow and DVC, the project strives to set a benchmark in precision medicine and diagnostic accuracy.

## Dataset
The dataset used for this project is sourced from Kaggle and comprises chest CT scan images, which are crucial for identifying and diagnosing chest cancer. You can access the dataset [here](https://www.kaggle.com/datasets/mohamedhanyyy/chest-ctscan-images).

## MLflow and MLOps Best Practices
A significant aspect of this project is implementing MLOps best practices. This includes:

- **MLflow for Model Lifecycle Management**: Leveraging MLflow for tracking experiments, packaging code into reproducible runs, and logging parameters, metrics, and output files.
- **Data Version Control (DVC)**: Using DVC to manage data and model files, ensuring reproducibility and trackability in the machine learning pipeline.
- **Standard ML Engineer Workflow**: Emphasizing the standard workflow of a Machine Learning Engineer, which involves iterative testing, data versioning, model tuning, and evaluation.

The project serves as a practical learning journey in mastering MLflow and DVC, highlighting the best practices in the field of MLOps.

## Deployment and Technologies

The deployment of this chest cancer classification model demonstrates a professional, scalable, and accessible approach to machine learning model deployment. The technologies used in this project include Docker, Flask, and AWS, each playing a critical role in ensuring the model's robustness and accessibility. 

### Docker
- **Containerization:** Docker is used to containerize the machine learning model along with its dependencies. This ensures consistency and reliability across various development and production environments, minimizing issues related to environment discrepancies.


### Flask
- **Web Server Interface:** Flask, a lightweight web framework, is employed to create a web server for the model. This setup allows users to interact with the model via HTTP requests, sending medical imaging data and receiving classification results.

### AWS
- **Cloud Deployment and Scaling:** The model is hosted on AWS (Amazon Web Services), demonstrating effective cloud deployment skills. AWS services enable the scalability of the application, ensuring it can handle varying loads and providing high availability.

### Integration and Workflow
- **End-to-End Workflow:** The integration of these technologies results in a streamlined workflow from model training to deployment. This section could include details about CI/CD pipelines, automated testing, or monitoring systems used in the project.

### User Interface
- **User-Friendly Interface:** If applicable, details about the user interface (UI) designed for interacting with the model. This could be a web portal, a dashboard, or an API endpoint documentation.
  

This detailed description of the deployment process and technologies underscores the project's commitment to delivering a professional-grade, user-friendly, and secure machine learning solution in the healthcare domain.


## How to Run

This guide provides step-by-step instructions to set up and run the "End-to-End Chest Cancer Classification using MLflow and DVC" project.

### Workflows

1. **Update Configuration Files:**
    - `config.yaml`: Update this file with the general configuration for the project.
    - `secrets.yaml` [Optional]: Update this file if there are any secrets or sensitive information required.
    - `params.yaml`: Adjust the parameters for the ML model or data processing steps.
    - Update the entity and configuration manager in `src/config`.

2. **Update Components and Pipeline:**
    - Update the components used in the project as necessary.
    - Modify the pipeline structure in `dvc.yaml`.
    - Update `main.py` with any changes in the execution logic.

3. **MLflow Setup:**
    - To view experiments and model tracking, run the MLflow UI locally using the command: `mlflow ui`.
    - For detailed MLflow usage, refer to the provided documentation or tutorial.

4. **Dagshub Setup:**
    - Set the MLflow tracking URI, username, and password as environment variables:
      ```
      export MLFLOW_TRACKING_URI=https://dagshub.com/entbappy/chest-Disease-Classification-MLflow-DVC.mlflow
      export MLFLOW_TRACKING_USERNAME=entbappy
      export MLFLOW_TRACKING_PASSWORD=[your_password]
      ```
    - Run your ML scripts, for example: `python script.py`.

5. **DVC Commands:**
    - Initialize DVC in your project: `dvc init`.
    - Reproduce the pipeline: `dvc repro`.
    - View the pipeline DAG: `dvc dag`.

### AWS CI/CD Deployment with GitHub Actions

1. **AWS Setup:**
    - Log in to the AWS console.
    - Create an IAM user with specific access:
      - EC2 access for virtual machine management.
      - ECR (Elastic Container Registry) access for Docker image storage.

2. **Deployment Process:**
    - Build and push the Docker image to ECR.
    - Launch an EC2 instance.
    - Pull the Docker image from ECR to the EC2 instance and launch it.

3. **GitHub Secrets Setup:**
    - Set up GitHub secrets for AWS credentials:
      - `AWS_ACCESS_KEY_ID`
      - `AWS_SECRET_ACCESS_KEY`
      - `AWS_REGION`
      - `AWS_ECR_LOGIN_URI`
      - `ECR_REPOSITORY_NAME`

4. **EC2 Configuration:**
    - Create an EC2 instance (preferably Ubuntu).
    - Install Docker on the EC2 instance.
    - Configure the EC2 instance as a self-hosted runner for GitHub Actions.

### Additional Information

- **About MLflow & DVC:**
    - MLflow is used for production-grade experiment tracking, logging, and tagging models.
    - DVC is a lightweight tool for proof of concept and experiment tracking, and can also handle pipeline orchestration.

By following these instructions, you should be able to set up, run, and deploy the chest cancer classification project successfully. Replace `[your_password]` with your actual MLflow tracking password and fill in other placeholders as per your project configuration.



## License


## Contact

