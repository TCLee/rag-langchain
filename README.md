# Build a Chatbot with LangChain

## Overview
The Jupyter notebook will go over an example of how to use [LangChain](https://python.langchain.com/v0.2/docs/introduction/) to design and implement an LLM-powered chatbot. This chatbot will be able to have a conversation and remember previous chats with a user.

The code in the notebook is adapted from the LangChain tutorial: [Build a Chatbot](https://python.langchain.com/v0.2/docs/tutorials/chatbot/)

## Setup

### Conda
1. You will need conda in order to install the required packages to run the notebook. [Installing conda](https://docs.conda.io/projects/conda/en/stable/user-guide/install/index.html).

2. Use your favourite terminal for the following steps. Create the environment from the [`environment.yml`](environment.yml) file:

```zsh
conda env create -f environment.yml
```

3. Activate the environment: 

```zsh
conda activate langchain-gemini
```

### Google Gemini API

The LLM that we will use in the notebook is Google's Gemini 1.5 Flash, since it offers a free tier for us to play around with.

To use the Gemini API, you'll need an API key. If you do not already have one, create a key in Google AI Studio.

[Get an API key](https://makersuite.google.com/app/apikey)

Assign your API key to an environment variable by running the following command in your terminal:

```zsh
export GOOGLE_API_KEY='YOUR_API_KEY'
```

### Jupyter Notebook

Creating the environment from the `environment.yml` file will install Jupyter Lab for you. Start Jupyter Lab from your terminal:

```zsh
jupyter lab
```

In Jupyter Lab, open the notebook `chatbot.ipynb` and follow the instructions there.