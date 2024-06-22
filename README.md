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

```brew install ollama```
Next check the version of installation:

```ollama -v```

And for me the output was: ollama version is 0.1.45

2. Prepare a Git Repository
Initialize a Git repository or clone an existing one. Create a folder named LLM_Integration to keep the local model separate from other deployments/projects.

3. Set Up a Python Environment
If you plan to add more to this project, set up a Python environment:


```python3 -m venv venv_llm```
```source venv_llm/bin/activate```

4. Download Docker and Pull the Docker Image for Ollama
Install Docker if you haven't already.

5: Pull the Ollama Docker image:

```docker pull ollama/ollama```

Run the Docker container:


```docker run -d -v ~/.ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama```

You can also run the image from Docker software.

5. Generate SSH Key
To resolve potential SSH key issues, follow these steps: Generate a new SSH key without a passphrase:

P.S. Press enter so you don't need to use a passkey, directly the model will be accessible which otherwise won't be if you give a passkey.

```ssh-keygen -t ed25519 -f ~/.ssh/id_ed25519 -C "balchandani.r@northeastern.edu"```

When prompted, leave the passphrase fields empty to remove the passphrase.

Copy the SSH key to the .ollama directory:

```mkdir -p ~/.ollama```
```cp ~/.ssh/id_ed25519 ~/.ollama/```

Set the OLLAMA_HOME environment variable:

```export OLLAMA_HOME=~/.ollama```
```echo 'export OLLAMA_HOME=~/.ollama' >> ~/.zshrc```

Ensure correct permissions for the SSH key:

```chmod 777 ~/.ollama/id_ed25519```

6. Run Ollama with Llama3 Model
Run the following command to start the Llama3 model:

```ollama run gemma:2b```

If you encounter an error related to the SSH key, such as input/output error, ensure that the SSH key is properly set up and the permissions are correct. If the issue persists, you may need to delete the existing container and recreate it using the Docker commands provided.




