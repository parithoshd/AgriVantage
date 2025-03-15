# Contributing to Agrivantage (Voice AI Assistant) 🌱📞

Thank you for your interest in contributing to **Agrivantage**, an AI-powered voice system for answering agricultural queries via Twilio! 🚀 Your contributions are valuable in making this project better.

---

## 📌 Prerequisites

Before you start, make sure you have the following installed:

- [Git](https://git-scm.com/downloads)
- [Python 3.9+](https://www.python.org/downloads/)
- [Node.js & npm](https://nodejs.org/en/download/)
- [ngrok](https://ngrok.com/download)
- [Twilio Account](https://www.twilio.com/try-twilio)
- [OpenAI API Key](https://platform.openai.com/signup/)
- [A GitHub account](https://github.com/)

---
## Features

- **Voice Call Handling:** Uses Twilio to record and process incoming voice calls.
- **Speech-to-Text:** Transcribes audio recordings using OpenAI’s Whisper API.
- **RAG Chain:** Answers agriculture-related questions by retrieving relevant information from local documents using LangChain and FAISS.
- **Dynamic NGROK Tunneling:** Automatically starts an ngrok tunnel for easy public access during development.
- **Document Processing:** Loads and splits PDF and text files from the `documents` directory to build a vector store.

## 💡 How to Contribute

### 1️⃣ Fork and Clone the Repository

1. Click the **Fork** button on the top right of this repository.
2. Clone your forked repository to your local machine:
   ```sh
   git clone https://github.com/YOUR_GITHUB_USERNAME/Agrivantage.git
   cd Agrivantage
3. Add the original repository as an upstream remote:
   ```sh
   git remote add upstream https://github.com/ORIGINAL_OWNER/Agrivantage-Voice-AI.git
### 2️⃣ Set Up Your Development Environment
1. Create an account from OpenAI, go to API Key then create your own API key, copy the api key and save to it in .env file.
2. Sign up for a Twilio account and then purchase a phone number by following Twilio's step-by-step instructions. After obtaining your number, navigate to the "Account Info" section on your dashboard and copy your Account SID and Auth Token.
3. Create a .env file in the root directory.
4. Add the following variables and update them with your actual API keys:
   ```sh
   OPENAI_API_KEY="your_openai_api_key"
   TWILIO_ACCOUNT_SID="your_twilio_account_sid"
   TWILIO_API_KEY_SECRET="your_twilio_auth_token"
### 3️⃣ Install Dependencies
1. Install all required dependencies:
   ```sh
   pip install -r requirements.txt
### 4️⃣ Setting Up ngrok
Install ngrok by first creating an account at ngrok.com. Once registered, go to the "Your Authentication" section, and then execute the following command in your terminal:
   ```sh
   ngrok config add-authtoken $YOUR_AUTHTOKEN
   ```
### 5️⃣ Run the Application
1. Start the FastAPI Server
   ```bash
   uvicorn main:app --host 0.0.0.0 --port 8000
2. Once ngrok is running, its generated URL will be stored in your .env file. Copy this URL for the next step.
3. Configure Twilio Webhook
   i.   Go to Twilio Console
   ii.  Navigate to Phone Numbers → Active Numbers.
   iii. Under Voice Configuration, paste the ngrok URL followed by /twilio/voice.   
   ```sh
   https://your-ngrok-url.ngrok-free.app/twilio/voice
5. Click Save
### 6️⃣ Check the Application
Make a call to the Twilio number you set up and follow the provided instructions.
### 6️⃣ Submitting a Contribution
📌 Creating a New Branch
Before making any changes, create a new branch:

```sh
git checkout -b feature/your-feature-name
```

🛠 Making Changes
Follow PEP8 guidelines for Python code.
Add comments where necessary.
Ensure the code is readable and well-structured.
✅ Testing Your Changes
Make sure the changes don’t break existing features:
   ```sh
   pytest
```

📤 Committing Your Changes
1. Stage your changes:
```sh
git add .
```
2. Commit with a meaningful message:
```sh
git commit -m "Added feature: Description of the feature"
```
3. Push to your fork:
```sh
git push origin feature/your-feature-name
```
### 🔃 Creating a Pull Request
1. Go to your repository on GitHub.
2. Click New Pull Request.
3. Select the main branch as the base and your feature branch as the compare branch.
4. Add a description of your changes.
5. Click Create Pull Request.

### 6️⃣ Code Review Process
1. A project maintainer will review your pull request.
2. Feedback may be given; please address any requested changes.
3. Once approved, your code will be merged into the main branch.

### Contribution Guidelines
- Open an issue before working on major changes.
- Be respectful when discussing in issues and pull requests.
- Keep pull requests small and focused on a single change.
- Write meaningful commit messages.

### Community & Support
- Join our GitHub Discussions for queries.
- Report issues using GitHub Issues.

Thank you for contributing to Agrivantage! 🎉🚀



