# Gen AI Projects

Jupyter notebooks exploring Generative AI with **LangChain**, **Hugging Face** and **LlamaIndex**.

| Notebook | What it does | Key needed |
|---|---|---|
| `Langchain_And_Huggingface.ipynb` | Calls Hugging Face models from LangChain: hosted (`HuggingFaceEndpoint`, Mistral-7B-Instruct) and local (`HuggingFacePipeline`, GPT-2) | `HF_TOKEN` |
| `RAG For Multiple Data Source.ipynb` | An agent that answers questions using three tools: Wikipedia, arXiv, and a FAISS vector search over the LangSmith docs | `OPENAI_API_KEY` |
| `test.ipynb` | Retrieval-augmented generation (RAG) over your own files with LlamaIndex, including saving and reloading the index | `OPENAI_API_KEY` |

## How to run (step by step)

You need **Python 3.10 or newer** ([download](https://www.python.org/downloads/)).

**1. Download the project**

```bash
git clone https://github.com/amitmohanty022/Gen-AI-Projects.git
cd Gen-AI-Projects
```

**2. Create a virtual environment and activate it**

```bash
python -m venv venv
# Windows
venv\Scripts\activate
# macOS / Linux
source venv/bin/activate
```

**3. Install the requirements**

```bash
pip install -r requirements.txt
```

This includes PyTorch for the local Hugging Face model, which is a large download (about 1–2 GB), so the first install takes a few minutes.

**4. Add your keys**

- OpenAI key: https://platform.openai.com/account/api-keys
- Hugging Face token (free): https://huggingface.co/settings/tokens
- Copy `.env.example` to a new file named `.env`
  - Windows: `copy .env.example .env`
  - macOS / Linux: `cp .env.example .env`
- Paste your keys after `OPENAI_API_KEY=` and `HF_TOKEN=`

**5. (For `test.ipynb` only) Add documents**

Put the PDFs or text files you want to ask questions about into the `data/` folder. For example, download the paper "Attention Is All You Need" from https://arxiv.org/abs/1706.03762.

**6. Start Jupyter**

```bash
jupyter notebook
```

Open a notebook and choose **Run → Run All Cells**.

### Running in Google Colab instead

1. Open the notebook on GitHub and click **Open in Colab**, or upload it at https://colab.research.google.com.
2. Click the 🔑 **Secrets** icon in the left sidebar and add `HF_TOKEN` and/or `OPENAI_API_KEY`.
3. Run the first cell. It installs the packages.

## Settings

| Variable in `.env` | Default | What it does |
|---|---|---|
| `OPENAI_API_KEY` | (empty) | OpenAI key |
| `OPENAI_MODEL` | `gpt-6-luna` | Chat model for the RAG notebooks |
| `HF_TOKEN` | (empty) | Hugging Face access token |

## Troubleshooting

| Problem | Fix |
|---|---|
| `AssertionError: Add OPENAI_API_KEY...` | Create the `.env` file (step 4) in the same folder as the notebooks, then restart the kernel. |
| `ValueError: No files found in data` | Add at least one file to `data/` (step 5). |
| Hugging Face `404` or "model not supported" | Change `repo_id` in the notebook to another instruct model from https://huggingface.co/models?inference_provider=all |
