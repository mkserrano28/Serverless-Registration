# Serverless-Registration

## Overview
I created an **e-commerce website** using **React.js** and **Tailwind CSS** and deployed it using **AWS serverless services**. This project includes:
- **CI/CD automation with AWS Amplify**
- **DynamoDB for user registration**
- **AWS Lambda for backend logic**
- **API Gateway to manage API requests**

🌍 **Live URL**: [https://main.d3o4gtrj4zyy3h.amplifyapp.com](https://main.d3o4gtrj4zyy3h.amplifyapp.com)  
🔗 **GitHub Repository**: [https://github.com/mkserrano28/serverless](https://github.com/mkserrano28/serverless)

---

## Steps to Deploy

### **1. Upload Project to GitHub**
I uploaded my project to a GitHub repository named **serverless**.  
🔗 [GitHub Repository](https://github.com/mkserrano28/serverless)

---

### **2. Deploy Frontend Using AWS Amplify**
I set up **AWS Amplify** to host my React.js project.  
📌 **CI/CD Enabled**: Every time I push updates to GitHub, **AWS Amplify automatically deploys the latest version** without manual intervention.

#### **AWS Amplify Deployment Screenshot**
![AWS Amplify Registration](Registration.png)

---

### **3. Create AWS Lambda for Backend Logic**
I developed an **AWS Lambda function** to handle backend processing and interact with DynamoDB.

#### **AWS Lambda Code and Deployment**
- The Lambda function is responsible for handling user registration.
- It processes API requests and stores data in **DynamoDB**.

📌 **Lambda Function Code Screenshot**  
![AWS Lambda](Lambda1.png)

📌 **Lambda Deployment (ZIP Upload)**  
`lambda_function.zip`

#### **Backend Logic Improvements**
To enhance **scalability, security, and efficiency**, here are some possible improvements:
 **Error Handling**: Implement detailed error responses (e.g., invalid inputs, DynamoDB errors).  
 **Validation Middleware**: Use **AJV** for JSON Schema validation before inserting into DynamoDB.  
 **Rate Limiting**: Protect API Gateway with AWS **WAF** or API rate limits to prevent abuse.  
 **Logging & Monitoring**: Use **AWS CloudWatch Logs** to track request failures and debugging.  

---

### **4. Set Up IAM Role & Policies**
To allow Lambda to interact with **DynamoDB**, I created an IAM role with the necessary permissions.

📌 **IAM Role Configuration Screenshot**  
![AWS IAM-Role](IAMRole.png)

📌 **IAM Policies for Lambda & DynamoDB**  
![AWS IAM-Policies](IAMPolicies.png)

---

### **5. Set Up API Gateway**
I created an **API Gateway** to manage and route API requests between my **Lambda function** and **DynamoDB**.

📌 **API Gateway Configuration Screenshots**  
![AWS API Gateway](API1.png)  
![AWS API Gateway](API2.png)  
![AWS API Gateway](API3.png)  
![AWS API Gateway](API4.png)  

---

### **6. Create DynamoDB for User Registration**
I configured **Amazon DynamoDB** to store user registration data. 

📌 **DynamoDB Table Screenshot**  
![AWS DynamoDB Data](DynamoDb1.png)

---

## **Technologies Used**
- **Frontend**: React.js, Tailwind CSS
- **Hosting & CI/CD**: AWS Amplify, GitHub
- **Backend**: AWS Lambda (Node.js)
- **Database**: Amazon DynamoDB
- **API Management**: Amazon API Gateway
- **Infrastructure**: Serverless Architecture

---

## **Future Enhancements**
- Implement authentication using **Amazon Cognito**.
- Add **GraphQL API** for more efficient data querying.
- Improve UI/UX for better user experience.

---

## **How to Run Locally**
1. **Clone the repository**:
   ```sh
   git clone https://github.com/mkserrano28/serverless.git
   cd serverless
