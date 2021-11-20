# Legal Summarization

## Prerequisites

- To run the code, ensure that you have a suitable version of Python (>= 3.6, < 3.7)
- If you have a Nvidia GPU with CUDA support, you can enable CUDA acceleration in the models. Make sure that the CUDA drivers are installed and PyTorch is able to find the correct GPU

## Installing Dependencies

To install dependencies, run

```bash
pip install -r requirements.txt
```

## Download Models

We use the following embedders:

1. Random BERT Embedder: Generates a random vector of size 768
2. BERT Base: Standard BERT embedder, finetuned on pacsum
3. Legal BERT: Finetuned on legal docs, performs better than non-generic models

To download the models, use the following links

- [Legal BERT](https://huggingface.co/nlpaueb/legal-bert-base-uncased/tree/main)
- [Pacsum Models]([https://drive.google.com/file/d/1wbMlLmnbD_0j7Qs8YY8cSCh935WKKdsP/view)

## Running the Code

To execute the code, after ensuring all dependencies and models are correct, use the following

```bash
python main.py
```

This will save the results into the `results` folder.

In order to tune the length of summaries, change the `SUMMARY_SIZE` parameter. It represents what percentage of the sentences to pick as summary (sorted by confidence scores). By default, it is set to 0.15
