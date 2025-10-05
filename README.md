# AI Water Quality Advisor
An AI powered web application that analyzes household water test results and provides safety assessments, possible issues, and treatment recommendations based on international water quality guidelines (WHO/EPA).

Built with AWS Cloud + AI to demonstrate cloud-native architecture, serverless design, and real-world AI integration.


# 🚀 Features
* User-Friendly Web App: Enter water test values (pH, turbidity, hardness, nitrates, etc.) via a responsive form.

* AI-Powered Analysis: Amazon Bedrock (Claude Sonnet 3.0) interprets results and generates recommendations.

* Cloud-Native Architecture: Serverless backend using AWS Lambda + GraphQL API Gateway (through AWS AppSync).

* Scalable Deployment: Frontend hosted on AWS Amplify.

* CI/CD: AWS Amplify's integration with Github facilitates a CI/CD pipeline to push latest code changes to te hosted application.

* Secure Access: AWS Cognito for user authentication and personal dashboards.



# 🏗️ Architecture

```

    [Frontend: React / Amplify] ←→ [Cognito]
        ↓
   [AppSync] (GraphQL API)
        ↓
   [Lambda Functions] → [Amazon Bedrock (AI Model)]
        ↓
   [DynamoDB] (store user inputs + AI reports)


```


# ⚙️ Tech Stack

* Frontend: React (Amplify-React UI and Hosting)
* Backend: AWS Lambda + API Gateway
* AI Model: Amazon Bedrock (Anthropic Claude Sonnet 3.0)
* Authentication: AWS Cognito


# 📊 Application Workflow

* User enters test results (e.g., pH 7.8, Turbidity 10 NTU, Hardness 250 mg/L).
* API Gateway forwards data to Lambda.
* Lambda formats a prompt and sends it to Bedrock.
* Bedrock returns structured insights:


# 🛠️ Setup & Deployment
Prerequisites:

* AWS account with Bedrock access enabled
* Node.js & npm (for frontend)
* AWS CLI configured
* A Github account

Steps:

1. Create new react application:

```
    npm create vite@latest ai-recipe-generator -- --template react-ts -y
    cd ai-recipe-generator
    npm install
    npm run dev

```

2. Install Amplify packages

```

npm create amplify@latest -y   

```

3. Initialise Github repository and push code to Github.

4. Deploy App with AWS Amplify.





# 🎯 Future Improvements

* Implement data persistence with DynamoDB to store test data and AI analysis.
* Add visual graphs for trends (Chart.js + DynamoDB data).
* Multi-language support (via Amazon Translate).
* Exportable PDF reports for users.


# 📌 Why This Project Matters

This project bridges environmental engineering and cloud AI, showing how AWS can support public health, sustainability, and data-driven decision-making.

It’s not just a coding demo — it’s a real-world application with potential impact.


# 👨‍💻 Author

Paul Onyebuchi

Cloud Developer | AWS Certified | Chemical Engineering Background
