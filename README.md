# HAGRID: A Human-LLM Collaborative Dataset for Generative Information-seeking with Attribution

<p align="center"><img src="https://github.com/project-miracl/hagrid/blob/main/assets/icon.png?raw=true" alt="HAGRID" width="20%"><br>
</p>

<p align="center">
    <a href="https://www.python.org/">
        <img alt="Build" src="https://img.shields.io/badge/Made%20with-Python-1f425f.svg?color=purple">
    </a>
    <a href="https://github.com/project-miracl/hagrid/blob/master/LICENSE">
        <img alt="License" src="https://img.shields.io/github/license/project-miracl/hagrid">
    </a>
    <a href="https://arxiv.org/abs/2307.16883">
        <img alt="arXiv" src="https://img.shields.io/badge/arXiv-2307.16883-b31b1b.svg">
    </a>
</p>

HAGRID (**H**uman-in-the-loop **A**ttributable **G**enerative **R**etrieval for **I**nformation-seeking **D**ataset) is a dataset for generative information-seeking scenarios.
It is constructed on top of [MIRACL 🌍🙌🌏](HTTP://miracl.ai), an information retrieval dataset that consists of queries along with a set of manually labelled relevant passages (quotes).

We collect attributed explanations for each question by eliciting prompts from [GPT-3.5](https://openai.com/blog/chatgpt), based on the given relevant passages. The explanations adhere to an in-context citation style, similar to scientific articles, that reference the supporting quotes.
We then ask human annotators to judge the explanations based on two criteria:
1. __Informativeness:__ whether they provide a direct answer to the question.
2. __Attributability:__ whether they are attributable to the source passages.

<img src="https://github.com/project-miracl/hagrid/blob/main/assets/workflow.jpg?raw=true" alt="HAGRID workflow" width="100%">

## Quick Links
  - [Data](#data)
  - [Baselines (coming soon!)](#baselines-coming-soon)
  - [Contact](#contact)
  - [License](#license)
  - [Citation](#citation)

## Data

HAGRID is hosted on Hugging Face 🤗: [link](https://huggingface.co/datasets/miracl/hagrid).

```python
import datasets
hagrid = datasets.load_dataset("miracl/hagrid", split="train")
print(hagrid[0])
```

|  Split | #Q | #A       | #Informativeness  | #Attribuatability       |
|:-----|:------:|:-------:|:------:|:-------:|
| Train     | 1,922 | 3,214 | 3,214 | 754 |
| Dev     | 716 | 1,318 | 1,157 | 826 |


## Baselines (Coming soon!)
We are planning to release baseline models soon! Stay tuned!

## Contact

If you have any questions, feel free to email us (project.miracl [at] gmail.com) or start a Github issue under this repository.


## License

This work is licensed under the Apache 2 license. See [LICENSE](LICENSE) for details.

## Citation
If you find this dataset and repository helpful, please cite HAGRID as follows:
```
@article{hagrid,
      title={{HAGRID}: A Human-LLM Collaborative Dataset for Generative Information-Seeking with Attribution}, 
      author={Ehsan Kamalloo and Aref Jafari and Xinyu Zhang and Nandan Thakur and Jimmy Lin},
      year={2023},
      journal={arXiv:2307.16883},
}
```
