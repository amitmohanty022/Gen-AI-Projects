# Gen AI Projects

Notebooks exploring generative-AI building blocks: running open models with Hugging Face and LangChain, building a multi-source RAG agent, and indexing documents with LlamaIndex.

**🔗 Run it live:** each notebook opens directly in Google Colab.

## Notebooks

| Notebook | What it covers | Run |
| --- | --- | --- |
| [Langchain_And_Huggingface.ipynb](https://github.com/amitmohanty022/Gen-AI-Projects/blob/main/Langchain_And_Huggingface.ipynb) | Calling Mistral-7B through `HuggingFaceEndpoint`, running GPT-2 locally with `HuggingFacePipeline`, and chaining prompts with LCEL | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amitmohanty022/Gen-AI-Projects/blob/main/Langchain_And_Huggingface.ipynb) |
| [RAG For Multiple Data Source.ipynb](https://github.com/amitmohanty022/Gen-AI-Projects/blob/main/RAG%20For%20Multiple%20Data%20Source.ipynb) | A tool-calling agent that answers from Wikipedia, arXiv and a FAISS index of the LangSmith docs | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amitmohanty022/Gen-AI-Projects/blob/main/RAG%20For%20Multiple%20Data%20Source.ipynb) |
| [test.ipynb](https://github.com/amitmohanty022/Gen-AI-Projects/blob/main/test.ipynb) | LlamaIndex: build, persist and query a vector index with a similarity cut-off | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/amitmohanty022/Gen-AI-Projects/blob/main/test.ipynb) |

## API keys

Put the keys you need in a `.env` file (or Colab **Secrets**):

```env
OPENAI_API_KEY=...     # RAG notebook and LlamaIndex notebook
HF_TOKEN=...              # Hugging Face notebook (Colab secret)
HUGGINGFACEHUBTOKEN=...   # same token, read by the Hugging Face notebook
```

## Run locally

```bash
git clone https://github.com/amitmohanty022/Gen-AI-Projects.git
cd Gen-AI-Projects
pip install -r requirements.txt jupyter
jupyter notebook
```

The notebooks use LangChain v1 (`langchain-core`, plus `langchain-classic` for the agent helpers), LlamaIndex (`llama_index.core`) and an OpenAI model (`gpt-6-luna`), because `gpt-3.5-turbo` was shut down on 23 October 2026.

## Author

**Amit Kumar Mohanty** · [GitHub](https://github.com/amitmohanty022) · [LinkedIn](https://www.linkedin.com/in/amitkrmohanty/)
