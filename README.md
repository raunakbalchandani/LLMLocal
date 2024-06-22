# LLMLocal
This project is created to store information related to Prompt Engineering. We are using the Ollama - Gemma 2b model to run locally on a macOS laptop.

# What is Ollama
Ollama is an open-source project designed to be a powerful and user-friendly platform for running LLMs on your local machine. It simplifies the complexities of LLM technology, making AI more accessible and customizable.

Here are the steps to explain how this model was integrated locally and used, helping save costs associated with paid versions of LLMs.

#Prequisites

Downloading OLLAMA file using Homebrew
Prepare a Git Repository and clone it locally
Make a folder LLM_Integration to keep the local model separate from other deployments/projects
Set up a Python environment if you plan to add more to this project
Download Docker and pull the Docker image for Ollama

#Why Choose Ollama:
Ollama has provided the access for multiple LLMs within one single application. Below are the reasons why I chose these two models.

Gemma (2B):Gemma 2b is used for generating high-quality, context-aware text responses in customer support chatbots to enhance user experience and efficiency.

Moondream 2 (1.4B) Use Cases: Basic conversational agents, personalized recommendations, simple chatbots. Details: Ideal for low-resource environments and applications that require basic interaction capabilities.

#Steps to Set Up and use Gemma model:

1. Download OLLAMA using Homebrew
Refer to this site to learn how to use Homebrew for downloading Ollama: https://formulae.brew.sh/formula/ollama

Use the VS Code terminal ot Mac to start downloading the Ollama model:

brew install ollama


