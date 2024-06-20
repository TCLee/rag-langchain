# Build a Retrieval Augmented Generation (RAG) App with LangChain

## Overview

One of the most powerful applications enabled by LLMs is sophisticated question-answering (Q&A) chatbots. These are applications that can answer questions about specific source information. These applications use a technique known as Retrieval Augmented Generation, or RAG.

This notebook will show how to build a simple Q&A application over a text data source using 
[LangChain](https://python.langchain.com/v0.2/docs/introduction/).

The code in the notebook is adapted from the following LangChain tutorials: 
- [Build a Retrieval Augmented Generation (RAG) Application](https://python.langchain.com/v0.2/docs/tutorials/rag/)
- [Build a Conversational RAG Application](https://python.langchain.com/v0.2/docs/tutorials/qa_chat_history/)


## Setup

### Conda
1. You will need conda in order to install the required packages to run the notebook. [Installing conda](https://docs.conda.io/projects/conda/en/stable/user-guide/install/index.html).

2. Use your favourite terminal for the following steps. 
   Make sure the current working directory is this cloned project's directory `rag-langchain`. For example:

   ```zsh
   cd /path/to/rag-langchain
   ```
   
3. Create the environment from the 
   [`environment.yml`](environment.yml) file:

    ```zsh
    conda env create -f environment.yml -p ./env
    ```

    This will create a new environment in a subdirectory of the project directory called `env`, (i.e., `rag-langchain/env`)

4. Activate the environment: 

    ```zsh
    conda activate ./env
    ```


### Google Gemini API

The LLM that we will use in the notebook is Google's Gemini 1.5 Flash, since it offers a free tier for us to play around with.

To use the Gemini API, you'll need an API key. If you do not already have one, create a key in Google AI Studio.

[Get an API key](https://makersuite.google.com/app/apikey)

Assign your API key to an environment variable by running the following command in your terminal:

```zsh
export GOOGLE_API_KEY="your-secret-key"
```


### LangSmith

Many of the applications you build with LangChain will contain multiple steps with multiple invocations of LLM calls. As these applications get more and more complex, it becomes crucial to be able to inspect what exactly is going on inside your chain or agent. The best way to do this is with [LangSmith](https://smith.langchain.com/).

After you sign up at the link above, make sure to set your environment variables to start logging traces: 

```zsh
export LANGCHAIN_TRACING_V2="true"
export LANGCHAIN_API_KEY="your-secret-key"
```

The `LANGCHAIN_API_KEY` is also used to fetch prompt templates from the [LangChain prompt hub](https://smith.langchain.com/hub/rlm/rag-prompt).


### Jupyter Notebook

The conda environment includes an installation of [Jupyter Lab](https://jupyter.org/). Start Jupyter Lab from your terminal:

```zsh
jupyter lab
```

In Jupyter Lab, open the notebook 
[`rag-langchain.ipynb`](rag-langchain.ipynb) 
and follow the instructions there.