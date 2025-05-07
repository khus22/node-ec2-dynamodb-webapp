# Node.js Web App with DynamoDB on AWS EC2 using Docker

This project demonstrates how to deploy a pre-built Node.js web application (pulled from Docker Hub) on an AWS EC2 instance using Docker. The application accepts user inputs (email/username) via a frontend form and stores them in a DynamoDB table.

---

## 🔧 Technologies Used

- **AWS EC2** – to host the application
- **AWS DynamoDB** – to store submitted user data
- **AWS IAM** – to provide secure programmatic access
- **Docker** – to run the pre-built Node.js application
- **Docker Hub** – source of the Node.js application image

---

## 🗂️ DynamoDB Table Setup

| Setting       | Value     |
|---------------|-----------|
| Table Name    | `Contacts`|
| Primary Key   | `id` (String)|

---

## 🔐 Required Environment Variables

Before running the container, set the following environment variables (from IAM credentials):

- `AWS_REGION` = `us-east-1`
- `AWS_ACCESS_KEY_ID` = your IAM access key
- `AWS_SECRET_ACCESS_KEY` = your IAM secret key

## 🔐 UI Screenshot

![UI Screenshot](https://github.com/khus22/node-ec2-dynamodb-webapp/blob/main/UI_Screenshot.png)


