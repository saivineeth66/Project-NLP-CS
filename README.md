## Setup
Obtain an OpenAI API key from https://platform.openai.com/api-keys. 
See the rate limits and usage. You need to buy credits. Because of huge number of API requests we make. 
Install the required Python package: pip install openai, func_timeout, datasets


## Running
Use the following command to run the code with the desired configurations:
python src/selection_math.py --start [start index] --end [end index] --dataset [dataset name] --backbone [ChatGPT or GPT-4] --cot_temperature [0 for greedy decoding, 0.5 for SC] --pal_temperature [0 for greedy decoding, 0.8 for SC] --sc_num [1 for greedy decoding. Others indicate SC samples.] --output_dir [output dir name] --key [OpenAI API Key] 


## Latest news-
You cannot implement Codex (code-davinci-002) as the API usage and model is deprecated from March23, 2023.  

## Citation

```bibtex
@inproceedings{zhao-etal-2023-automatic,
    title = "Automatic Model Selection with Large Language Models for Reasoning",
    author = "Zhao, James  and
      Xie, Yuxi  and
      Kawaguchi, Kenji  and
      He, Junxian  and
      Xie, Michael",
    editor = "Bouamor, Houda  and
      Pino, Juan  and
      Bali, Kalika",
    booktitle = "Findings of the Association for Computational Linguistics: EMNLP 2023",
    month = dec,
    year = "2023",
    address = "Singapore",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2023.findings-emnlp.55",
    doi = "10.18653/v1/2023.findings-emnlp.55",
    pages = "758--783",
    abstract = "Chain-of-Thought (CoT) and Program-Aided Language Models (PAL) represent two distinct reasoning methods, each with its own strengths. CoT employs natural language, offering flexibility and interpretability, while PAL utilizes programming language, yielding more structured and rigorous logic. We introduce a model selection method to combine the best of both worlds by employing a large language model (LLM) to dynamically select between them. Our theoretical analysis underscores the feasibility of this method, which is further corroborated by empirical results. Our proposed method demonstrates significant performance improvements across eight reasoning datasets with Codex, ChatGPT, and GPT-4. Additionally, our method is complementary to self-consistency; when integrated, it can further enhance performance while significantly reducing computation costs. Moreover, we achieve new state-of-the-art results on GSM8K and SVAMP, with respective accuracies of 96.8{\%} and 93.7{\%}.",
}

```


