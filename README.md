# ICSE 2025 CLDK Tutorial

In this hands on session we will explore the CLDK and its capabilities with a few real-world examples of using the CLDK and LLMs to build:

1. a code summarization tool: See [Code Summarization](./1-codesummary.ipynb)
2. a test generation tool: See [Test Generation](./2-testgeneration.ipynb)

## 1.  Prerequisites

1. Install CLDK and java bindings. Detailed set-up instructions can be found in the [CLDK documentation](https://codellm-devkit.info/installing/#java-analysis).
2. An openrouter API key to access some opensource LLMs. If you don't have an account, you can sign up for free at [openrouter.ai/sign-up](https://openrouter.ai/sign-up).


## 2. Tutorial setup

1. First, let's clone this repository and navigate to the directory:

   ```bash
   git clone https://github.com/codellm-devkit/cldk-tutorial.git && \
   cd cldk-tutorial
   ```

2. Next, create a `.env` file in the root directory.

   ```bash
   touch .env
   ```

### Create openrouter API key

Log in to your openrouter account and create a new [API key](https://openrouter.ai/settings/keys). 

![Image](https://github-production-user-asset-6210df.s3.amazonaws.com/1433964/439037039-9a72147c-0306-4a6e-81c1-2bd20012edd8.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250430%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250430T014851Z&X-Amz-Expires=300&X-Amz-Signature=5b4d214f31b63f4c9dcac4b9bbc74db83bf035afefd3082eb1935eedf2b71aa1&X-Amz-SignedHeaders=host)
   **Fig 1. Click "Create Key"**

![Image](https://github-production-user-asset-6210df.s3.amazonaws.com/1433964/439037040-93055b55-b619-4686-91c7-11d579934ae7.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250430%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250430T014833Z&X-Amz-Expires=300&X-Amz-Signature=effa8976f088cbd495f8fb4aa51777caad04a050095a7097aa1387b9af2a89b9&X-Amz-SignedHeaders=host)
   **Fig 2.Generate a name and click "Create"**


![Image](https://github-production-user-asset-6210df.s3.amazonaws.com/1433964/439037041-f2b9ee06-e54d-4ceb-84ed-140b18daa6d9.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20250430%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20250430T014905Z&X-Amz-Expires=300&X-Amz-Signature=566299dc78cc646fb3d8b83716e2308168e2e9dd645a58308ffc4ccccfa3b330&X-Amz-SignedHeaders=host)
   **Fig 3. Copy the API key**

Copy the API key and paste it into the `.env` file as follows:

```bash
# .env
OPENROUTER_API=sk-rest-of-your_api_key-here
# Ensure to replace 'sk-rest-of-your_api_key-here' with your actual API key
```

### Install dependencies and requirements
Finally, let's install the required dependencies. You can do this by running the following command in your terminal:

   ```bash
   pip install -r requirements.txt
   ```