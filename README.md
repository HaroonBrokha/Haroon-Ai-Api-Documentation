# 🚀 **Haroon AI API - Powered by Gemini**

This is the **Haroon AI API**, a custom AI-powered content generation API designed to interact with **Google Gemini**. It allows users to send prompts and receive AI-generated content, with custom handling and failover mechanisms for maximum reliability. The API is built with flexibility, scalability, and security in mind.

This API is **publicly available** for integration into web and mobile applications, and it provides an advanced **AI response generation** system, including automatic metadata watermarking and secure API key handling.

---

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=node.js&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Vercel](https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white)
![Firebase](https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=for-the-badge&logo=mongodb&logoColor=white)
![Redis](https://img.shields.io/badge/Redis-DC382D?style=for-the-badge&logo=redis&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Nginx](https://img.shields.io/badge/Nginx-269539?style=for-the-badge&logo=nginx&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![CI/CD](https://img.shields.io/badge/CI/CD-4CAF50?style=for-the-badge&logo=continuousintegration&logoColor=white)
![Markdown](https://img.shields.io/badge/Markdown-000000?style=for-the-badge&logo=markdown&logoColor=white)
![VS Code](https://img.shields.io/badge/VS%20Code-007ACC?style=for-the-badge&logo=visualstudiocode&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![Insomnia](https://img.shields.io/badge/Insomnia-4000BF?style=for-the-badge&logo=insomnia&logoColor=white)
![REST API](https://img.shields.io/badge/REST_API-02569B?style=for-the-badge&logo=rest&logoColor=white)
![JSON](https://img.shields.io/badge/JSON-000000?style=for-the-badge&logo=json&logoColor=white)
![Heroku](https://img.shields.io/badge/Heroku-430098?style=for-the-badge&logo=heroku&logoColor=white)
![GraphQL](https://img.shields.io/badge/GraphQL-E10098?style=for-the-badge&logo=graphql&logoColor=white)
![Swagger](https://img.shields.io/badge/Swagger-85EA2D?style=for-the-badge&logo=swagger&logoColor=black)
![Jest](https://img.shields.io/badge/Jest-C21325?style=for-the-badge&logo=jest&logoColor=white)
![Mocha](https://img.shields.io/badge/Mocha-8D6748?style=for-the-badge&logo=mocha&logoColor=white)
![Chai](https://img.shields.io/badge/Chai-A30701?style=for-the-badge&logo=chai&logoColor=white)
![Yarn](https://img.shields.io/badge/Yarn-2C8EBB?style=for-the-badge&logo=yarn&logoColor=white)
![NPM](https://img.shields.io/badge/NPM-CB3837?style=for-the-badge&logo=npm&logoColor=white)
![Axios](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)
![CORS](https://img.shields.io/badge/CORS-FF6F00?style=for-the-badge&logo=cors&logoColor=white)


## 🔑 **API Overview**

The **Haroon AI API** is designed to allow users to send AI prompts, process them through the **Google Gemini AI Model**, and receive rich text-based responses with project metadata included.

Key features:
- **Custom AI Prompt Handling:** Automatically includes the project name and developer information in every AI request.
- **Robust Failover Mechanism:** Automatically retries with multiple Google Gemini API keys until a successful response is received.
- **Metadata Watermarking:** Each response contains project metadata, ensuring that all AI-generated content is attributed to the "Haroon AI" system.

---

## 📋 **Features & Benefits**

- **Seamless Integration:** Easily integrate with your website or app to generate AI content on-demand.
- **Customizable Prompting:** Allow users to guide the AI with custom instructions.
- **Multi-API Key Support:** Redundancy with multiple Google Gemini API keys to avoid downtime.
- **Security:** Supports POST requests with user-supplied API keys and prompts. Access is restricted to specific domains for enhanced security.

---

## 🌐 **API Endpoint**

### **POST Endpoint**:
```
https://haroon-ai-api-public.vercel.app/api/haroonai
```

---

## 🛠️ **Request Parameters**

### **Required Parameters**:
- **`prompt`**: The text prompt or instruction to send to the AI. (e.g., "What is AI?")
- **`api`**: Your Google Gemini API key for authenticating the request.

### **Request Format**:
- **Content-Type:** `application/json`
- **Method:** `POST`

---

## 📝 **Sample Request (POST)**

### **Request Payload Example**:

```json
{
  "prompt": "Hello, who are you?",
  "api": "YOUR_GOOGLE_GEMINI_API_KEY"
}
```
-- **Replace YOUR_GOOGLE_GEMINI_API_KEY with your personal API key for Google Gemini.**

## **📄 API Response Format**
-- **After sending a request, you will receive the AI-generated content in the following JSON structure:**

```
{
  "success": true,
  "message": "AI response fetched successfully.",
  "response": "Hello, I am Haroon AI, developed by Haroon Brokha. How can I assist you today?",
  "metadata": {
    "author": "Haroon Brokha",
    "website": "https://github.com/haroonbrokha",
    "project": "Haroon AI API",
    "description": "Custom AI-powered API for generating content with Google Gemini, including failover and metadata watermarking."
  }
}
```
## 📄 **API Response Fields**

### **Response Fields:**
- **`success`**: A boolean indicating whether the request was successful.
- **`message`**: A descriptive message about the API response.
- **`response`**: The AI-generated content.
- **`metadata`**: Contains project details (e.g., author, website, project description).

---

## 🛡️ **Security and Privacy**

The API supports secure POST requests and allows users to pass their API keys via request parameters. The following security measures are in place:

- **CORS Restriction**: The API is accessible from all domains (e.g., `https://storefy-x.vercel.app`).
- **API Key Protection**: API keys are provided by users via query parameters and never stored in the codebase.
- **Data Privacy**: All user-provided data (prompts) is processed on-the-fly and not stored for future use.

---

## 🔄 **API Keys and Failover Mechanism**

The **Haroon AI API** supports the use of multiple Google Gemini API keys to ensure high availability and prevent failures:

- **Automatic API Key Rotation**: The API will automatically attempt to use the next available API key if the current one fails.
- **Retry Mechanism**: The system will continue trying available keys until a valid response is received from Google Gemini.

### **Example keys used:**
- `AIzaSyA8ZhmFMXSyKim6Naz0-*****`
- `AIzaSyDL2g2pyov2a0mX8VYyMlhfA*****`
- And more…

---
🔑 **Get Your Gemini API Key**  
To use the Haroon AI API, you will need a valid Gemini API key. You can get your API key from the Google AI Studio.

1. Visit [AI Studio - Google Gemini API](https://aistudio.google.com/app/apikey).
2. Follow the instructions to sign up or log in to your Google account.
3. Generate your API key for use with the Haroon AI API.

Once you have your API key, you can use it in your requests to the Haroon AI API.

---
## 💻 **Example Integration (JavaScript)**

### **JavaScript (Client-Side) Example:**

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Haroon AI Test</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <style>
    /* Custom Glass Effect */
    .glass {
      backdrop-filter: blur(10px);
      background: rgba(255, 255, 255, 0.1);
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1), 0 1px 3px rgba(0, 0, 0, 0.08);
    }

    /* Gradient Background */
    .gradient-bg {
      background: linear-gradient(135deg, rgba(85, 58, 233, 1) 0%, rgba(0, 212, 255, 1) 100%);
    }
  </style>
</head>
<body class="gradient-bg font-sans">

  <div class="flex justify-center items-center min-h-screen p-4">
    <div class="glass w-full sm:w-96 max-w-md">
      <h1 class="text-4xl font-extrabold text-center text-white mb-6">Haroon AI Test</h1>

      <div class="space-y-4">
        <!-- User Input -->
        <div>
          <label for="userPrompt" class="text-lg font-medium text-white">Ask me anything...</label>
          <input type="text" id="userPrompt" class="w-full mt-2 px-4 py-3 bg-transparent border-2 border-gray-200 text-white rounded-lg focus:outline-none focus:ring-2 focus:ring-blue-500 placeholder-gray-400" placeholder="Type your prompt here..." />
        </div>

        <!-- Submit Button -->
        <button id="submitBtn" class="w-full py-3 bg-gradient-to-r from-blue-500 to-cyan-400 text-white font-semibold rounded-lg hover:bg-gradient-to-l transition duration-300 transform hover:scale-105 ease-in-out">Submit</button>
      </div>

      <!-- Response Output -->
      <div class="mt-6">
        <h2 class="text-xl font-medium text-white">AI Response:</h2>
        <pre id="response" class="mt-2 bg-gray-800 bg-opacity-50 text-white p-4 rounded-lg text-sm h-48 overflow-auto border border-gray-300"></pre>
      </div>
    </div>
  </div>

  <script>
    document.getElementById('submitBtn').addEventListener('click', async function () {
      const prompt = document.getElementById('userPrompt').value;
      const apiKey = 'YOUR_GOOGLE_GEMINI_API_KEY'; // Replace with your API key

      // Clear previous response
      document.getElementById('response').textContent = 'Loading...';

      const response = await fetch('https://haroon-ai-api-public.vercel.app/api/haroonai', {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
        },
        body: JSON.stringify({ prompt, api: apiKey })
      });

      const data = await response.json();
      document.getElementById('response').textContent = JSON.stringify(data, null, 2);
    });
  </script>

</body>
</html>

```
This code provides a simple front-end example for submitting user prompts to the Haroon AI API and displaying the AI-generated response.

##📦 **Deployment**  

To deploy the Haroon AI API to platforms like Vercel:

1. Clone or fork this repository.
2. Set up the environment variables (if necessary) and API keys securely.
3. Deploy to your chosen platform (e.g., Vercel, Heroku, etc.).
4. Once deployed, your API will be publicly available to integrate into your applications.

##🧑‍💻 **About the Developer**  

Haroon Brokha is the developer behind this project.  
For more details on future projects or to connect, visit my GitHub Profile.

##📃 **License**  

This project is licensed under the MIT License. See the LICENSE file for more details.

##🤝 **Contributions**  

Feel free to contribute! Whether you have suggestions, bug fixes, or new features to add, all contributions are welcome. Please follow the standard GitHub pull request workflow.

##📧 **Contact**  
Author: Haroon Brokha   
GitHub: @haroonbrokha  
Website: haroonbrokha.com

