# Building-LLM-Workflows-From-Basic-to-Advanced
This project implements LLM (Large Language Model) workflows for repurposing blog content into summaries, social media posts, and email newsletters. The workflows include:
* Pipeline Workflow: A sequential workflow that processes tasks one after another.
* Workflow with Reflexion: A self-correcting workflow that improves the quality of generated content.
* Agent-Driven Workflow: A dynamic workflow where an LLM agent decides the order of tasks.

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Setup Instructions](#setup-instructions)
3. [Running the Code](#running-the-code)
4. [Workflow Details](#workflow-details)

## Prerequisites
Before running the code, ensure you have the following:
* Python 3.10+: The code is written in Python and requires Python 3.10 or higher.
* OpenAI API Key: You need an API key from OpenAI to make API calls.
* Required Python Libraries:
    * openai: For interacting with the OpenAI API.
    * python-dotenv: For loading environment variables from a .env file.
    * requests: For making HTTP requests (already included in Python's standard library).
Install the required libraries using pip:
```
pip install openai python-dotenv
```

## Setup Instructions
1. Clone the Repository:
    ```
    git clone https://github.com/your-username/llm-workflow-assignment.git
    cd llm-workflow-assignment
    ```
2. Create a .env File:
    Create a .env file in the project directory and add your OpenAI API key and other configurations:
    ```
    API_KEY=your_openai_api_key
    BASE_URL=https://api.openai.com/v1
    LLM_MODEL=gpt-4
    MODEL_SERVER=OPENAI
    ```
    Replace your_openai_api_key with your actual OpenAI API key.<br>
3. Add Sample Blog Post:
   Save the sample blog post in a file named sample-blog-post.json in the project directory. Example content:
  ```
    {
      "title": "The Impact of Artificial Intelligence on Modern Healthcare",
      "content": "Artificial intelligence (AI) is revolutionizing the healthcare industry...",
      "author": "Dr. Sarah Johnson",
      "date_published": "2025-03-10",
      "tags": ["healthcare", "artificial intelligence", "technology", "medicine"]
    }
  ```
## Running the Code
Run the script using the following command:
```
python llm_workflow.py
```
## What Happens When You Run the Code
1. The script reads the blog post from sample-blog-post.json.
2. It processes the blog post using three workflows:
    * Pipeline Workflow: Generates a summary, social media posts, and an email newsletter sequentially.
    * Workflow with Reflexion: Enhances the quality of the generated content using self-correction.
    * Agent-Driven Workflow: Uses an LLM agent to dynamically decide the order of tasks.
3. The results of each workflow are printed to the console in JSON format.

## Workflow Details
1. Pipeline Workflow
* Tasks:
    * Extract key points from the blog post.
    * Generate a summary from the key points.
    * Create social media posts for Twitter, LinkedIn, and Facebook.
    * Create an email newsletter.

* Output: A dictionary containing the summary, social media posts, and email newsletter.

2. Workflow with Reflexion
* Tasks:
    * Extract key points with self-correction.
    * Generate a summary with self-correction.
    * Create social media posts with self-correction.
    * Create an email newsletter with self-correction.

* Output: A dictionary containing the improved summary, social media posts, and email newsletter.

3. Agent-Driven Workflow
* Tasks:
    * The LLM agent decides the order of tasks dynamically.
    * The agent uses tools to extract key points, generate a summary, create social media posts, and create an email newsletter.

* Output: A dictionary containing the final results or an error message if the workflow fails.
