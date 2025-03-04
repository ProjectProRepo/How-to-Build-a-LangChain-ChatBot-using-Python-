# LLM Chatbot with Memory (LangChain + Gradio + Mistral 7B)

This project is a retrieval-augmented chatbot built using LangChain, Gradio, and Mistral 7B. It supports conversational memory and runs efficiently on Google Colab.

## Features

- Uses Mistral 7B, an open-source LLM from Hugging Face  
- Integrates LangChain for conversation management and memory  
- Provides a Gradio web-based chat UI for interaction  
- Implements conversational memory to remember past chats  

## Installation

Run the following command to install the required dependencies:

```bash
pip install -q langchain transformers accelerate bitsandbytes gradio langchain_community
```

## Setup

Before running the chatbot, set up your Hugging Face token:

```python
import os
os.environ["HUGGING_FACE_HUB_TOKEN"] = "your_huggingface_token_here"
```

## Model and Pipeline

The chatbot loads the **Mistral 7B** model from Hugging Face and creates a text generation pipeline.

## Conversational Memory

LangChain's **ConversationBufferMemory** is used to retain chat history, ensuring the chatbot can remember previous interactions.

## Running the Chatbot

The chatbot is deployed using **Gradio**, providing an interactive UI. Run the script and access the chat interface through the generated Gradio link.

## Usage

1. Run the script in **Google Colab** or locally.  
2. Interact with the chatbot through the **Gradio web UI**.  
3. Ask multiple questions – it **remembers past interactions**.  
4. Type `"exit"` to stop the chat session.  

## Notes and Considerations

- Ensure your **Hugging Face token** is valid before running the script.  
- If running on **Google Colab**, enable **GPU acceleration** (`Runtime → Change runtime type → GPU`).  
- The chatbot's **memory resets** when you restart the script.  

## Acknowledgments

- **[LangChain](https://python.langchain.com/)** – Conversational AI framework  
- **[Gradio](https://www.gradio.app/)** – UI for AI models  
- **[Hugging Face](https://huggingface.co/)** – Open-source LLMs like **Mistral 7B**  
