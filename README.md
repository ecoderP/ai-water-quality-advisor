# ai-water-quality-advisor
An Ai powered web application that analyzes household water test results and provides safety assessments, possible issues, and treatment recommendations based on international water quality guidelines (WHO/EPA).

Built with AWS Cloud + AI to demonstrate cloud-native architecture, serverless design, and real-world AI integration.

# 🚀 Features
User-Friendly Web App: Enter water test values (pH, turbidity, hardness, nitrates, etc.) via a responsive form.

AI-Powered Analysis: Amazon Bedrock (Claude Sonnet 3.0) interprets results and generates recommendations.

Cloud-Native Architecture: Serverless backend using AWS Lambda + API Gateway.

Data Persistence: Stores test history and AI analysis in DynamoDB.

Scalable Deployment: Frontend hosted on AWS Amplify.

Secure Access: AWS Cognito for user authentication and personal dashboards.

# 🏗️ Architecture

```
    [Frontend: React / Amplify]
        ↓
   [API Gateway]
        ↓
   [Lambda Functions] → [Amazon Bedrock (AI Model)]
        ↓
   [DynamoDB] (store user inputs + AI reports)


```