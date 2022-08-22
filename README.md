<h1 align="center">Welcome to question-generator 👋</h1>
<p>
  <a href="#" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-yellow.svg" />
  </a>
</p>

This repo contains simplified question generator model pipeline. This is a part of [Quizzy](https://github.com/Karthick47v2/quizzzy/tree/main) project, you can see the model in action there. Generating questions by finetuning T5 transformer on both SQuAD and SciQ datasets. PyTorch Lightning is used to finetune transformer. `Context`, `Question` and `Answer` extracted from datasets. `Context` and `Answer` will be given to model as input in order to generate `Question`. SQuAD is a reading comprehension dataset, model trained on that dataset is used for general purpose question generation and SciQ contains science exam questions and context, model trained on that dataset used specifically for physics, chemistry and biology related question generation on [Quizzy](https://github.com/Karthick47v2/quizzzy/tree/main) application.

### Transformer model input

```
"context: {context} answer: {answer}"
```

### Prerequisite

- Python 3.7 or newer.

## Dataset

- **[The Standford Question Answering Dataset - SQuAD](https://rajpurkar.github.io/SQuAD-explorer/)**
- **[SciQ Dataset](https://allenai.org/data/sciq)**

## Usage

> All dataset links available in notebook. SciQ dataset contains context related to Physics, Chemistry and Biology exam questions with context and SQuAD datast is a reading comprehension dataset. So, choose a dataset suitable for you.

- Export training dataset from `data_extraction.ipynb`.
- Run `train.ipynb` to start training.

> Skip ONNX conversion and quantization steps if you are using GPU for inference. [fastT5](https://github.com/Ki6an/fastT5) is used to convert PyTorch model to ONNX which only supports CPU version of onnxruntime currently.

## Author

👤 **Karthick T. Sharma**

- Github: [@Karthick47v2](https://github.com/Karthick47v2)
- LinkedIn: [@Karthick47](https://linkedin.com/in/Karthick47)

## Citation

### SQuAD

```
@inproceedings{rajpurkar-etal-2016-squad,
    title = "{SQ}u{AD}: 100,000+ Questions for Machine Comprehension of Text",
    author = "Rajpurkar, Pranav  and
      Zhang, Jian  and
      Lopyrev, Konstantin  and
      Liang, Percy",
    booktitle = "Proceedings of the 2016 Conference on Empirical Methods in Natural Language Processing",
    month = nov,
    year = "2016",
    address = "Austin, Texas",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/D16-1264",
    doi = "10.18653/v1/D16-1264",
    pages = "2383--2392",
}
```

### SciQ

```
@inproceedings{SciQ,
    title={Crowdsourcing Multiple Choice Science Questions},
    author={Johannes Welbl, Nelson F. Liu, Matt Gardner},
    year={2017},
    journal={arXiv:1707.06209v1}
}
```

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/Karthick47v2/question-generator/issues).

## Show your support

Give a ⭐️ if this project helped you!
