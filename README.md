# Streamlit Chatbot with Memory using Llama-2-7B-Chat (Quantized GGML)

Working Url: https://chatdemo.talhaanwar.com/ 


## Table of Contents

- [Introduction](#introduction)
- [Project Overview](#project-overview)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Docker Compose](#docker-compose)
- [Acknowledgments](#acknowledgments)

## Introduction

Welcome to the **Streamlit Chatbot with Memory using Llama-2-7B-Chat (Quantized GGML)** repository! This project aims to provide a simple yet efficient chatbot that can be run on a CPU-only low-resource Virtual Private Server (VPS). The chatbot is powered by the Llama-2-7B-Chat model, which has been quantized for better performance on resource-constrained environments. The web application is built using Streamlit, making it user-friendly and easy to interact with.

The main inspiration for this project comes from the need to have a chatbot capable of maintaining some context or memory during conversations, making the chat experience more natural and engaging for users. With the quantized GGML version of the Llama-2-7B-Chat model, we can leverage powerful language generation capabilities without the need for specialized hardware.

## Project Overview

The repository contains all the necessary code and files to set up and run the Streamlit Chatbot with Memory using the Llama-2-7B-Chat model. Here's a brief overview of the key components:

- `app.py`: The Streamlit web application code that allows users to interact with the chatbot through a simple user interface.

- `llama-2-7b-chat.ggmlv3.q2_K.bin`:  Quantized model weights provided by TheBloke.   Can be download via wget or manually  

```
!wget https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/resolve/main/llama-2-7b-chat.ggmlv3.q2_K.bin
```

- `Dockerfile`: The Dockerfile used to containerize the application for easy deployment and management.

- `docker-compose.yml`: A Docker Compose file that simplifies the deployment of the chatbot with memory as a Docker container.

- `requirements.txt`: Contains a list of Python dependencies required to run the application.

## Prerequisites

Before running the Streamlit Chatbot with Memory, you need to have the following installed:

1. Python (version 3.6 or higher)
2. Docker (if you plan to use the Docker Compose setup)

## Installation

To set up the chatbot locally, follow these steps:

1. Clone this repository to your local machine using Git:

```bash
git clone https://github.com/talhaanwarch/streamlit-llama.git
cd streamlit-chatbot-memory
```

2. Create a virtual environment (optional but recommended) and activate it:

```bash
python -m venv venv
source venv/bin/activate  
```

3. Install the required Python packages:

```bash
pip install -r requirements.txt
```

## Usage

To run the Streamlit Chatbot with Memory, execute the following command:

```bash
streamlit run app.py
```

This will start the Streamlit server, and you can access the chatbot interface by opening your web browser and navigating to `http://localhost:8501`.

Simply type your messages in the input box and press "Enter" to send them to the chatbot. The chatbot will respond based on the context of the conversation, thanks to its memory capabilities.

## Docker Compose

If you prefer to deploy the chatbot using Docker Compose, follow these steps:

1. Make sure you have Docker and Docker Compose installed on your system.

2. Start the container using Docker Compose:

```bash
docker-compose up -d
```

The chatbot will be accessible at `http://localhost:8501` in your web browser.

## Acknowledgments

- Streamlit Chatbot code credits go to [Data Professor](https://github.com/dataprofessor). Their original repository can be found [here](https://github.com/dataprofessor/streamlit_chatbot).

- Quantized GGML version of Llama-2-7B-Chat credits go to [TheBloke](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML).

Thank you for your interest in this project. Feel free to contribute, report issues, or provide feedback. Happy chatting!
