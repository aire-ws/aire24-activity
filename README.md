# AIRE'24 Joint Activity

[![GitHub](https://img.shields.io/github/license/aire-ws/aire24-activity)](./LICENSE)

This repository contains the material for the joint activity during the [Eleventh International Workshop on Artificial Intelligence and Requirements Engineering (AIRE'24)](https://aire-ws.github.io/aire24/) (co-located with the [32nd Requirements Engineering (RE) Conference](https://conf.researchr.org/home/RE-2024) in Iceland).

## Activity Description

The purpose of the activity is to investigate the following hypothesis:

> Have large-language models (LLMs) made previous AI tools obsolete?

The AIRE workshop series has - similar to comparable venues like the [Natural Language Processing for Requirements Engineering (NLP4RE) workshops](https://nlp4re.github.io/2024/) - brought forth many interesting AI- and ML-powered tools.
These tools were often meticulously designed, authors collected and annotated training data manually, and tools were trained locally with much effort.
But the wake of LLMs and generative AIs (GenAIs) like [ChatGPT](https://chat.openai.com/) or [Llama](https://llama.meta.com/) has put all this effort into question.

These tools can perform several requirements engineering related tasks out of the box, without any design, and barely any data preparation or training.
Was all previously invested effort obsolete?
In this activity, we invite to explore this hypothesis.
The activity is neither systematic nor conclusive, but shall rather stimulate discussions about the topic.
Feel free to extend or change it.

## Activity Instructions

To participate in the joint activity, *fork this repository* and please follow these steps.

### 1. Select a Study

Select a (published) study that presents an AI-supported tool that performs an RE task.
The study should clearly describe the task of the tool, contain a public replication package that includes an evaluation of the tool, and contain a data set used in the evaluation comprision of (1) input data, (2) expected outcome (i.e., ground truth), and (3) the tool output.

We have prepared some studies for this task which are readily available:

1. The **CiRA tool** by Frattini et al.[^1] (located in [studies/aire-23-frattini/](./studies/aire-23-frattini/)): a BERT-based tool that automatically generates test case descriptions from conditional requirements sentences.
2. The **ILLOD** tool by Hasso et al.[^2] (located in [studies/refsq-22-hasso/](./studies/refsq-22-hasso/README.md)): a custom tool for detecting abbreviation-expansion pairs in technical documents.

All prepared studies contain a dedicated `README.md` file with some additional information.
You can also use an own study of your choice.
In this case, simply copy the [studies/template/](./studies/template/) folder and fill in the respective information.

### 2. Select Data

From the selected study, choose data points from its empirical evaluation. 
The data points should consist of the input data provided to the tool, the expected output (i.e., the ground truth), and the output that the tool produced.
All prepared studies already contain pre-selected data points.

### 3. Engineer a Prompt

Now, pick an LLM of your choice (e.g., OpenAI's [ChatGPT](https://chat.openai.com/)) and try to perform the same task that the tool is performing just by providing the input data and a prompt.
Document the selected LLM, your prompts, and the output of the LLM produced in the respective markdown file.

### 4. Reflect

Based on the experiences with the LLM performing the tool’s task, reflect on the following questions:

- What did the LLM excel at?
- What did the LLM struggle with?
- Have our previously developed AIRE tools become obsolete?

Feel free to add questions and insights of your own.

## License

Copyright © 2025 of the ILLOD study under studies/refsq-22-hasso by Hussein Hasso.
Copyright © 2024 of the rest of the repository by Julian Frattini, Chetan Arora, and Fatma Basak Aydemir.
This work (source code) is available under [MIT license](./LICENSE).

[^1]: Frattini, J., Fischbach, J., & Bauer, A. (2023, September). CiRA: An Open-Source Python Package for Automated Generation of Test Case Descriptions from Natural Language Requirements. In 2023 IEEE 31st International Requirements Engineering Conference Workshops (REW) (pp. 68-71). IEEE. DOI: [10.1109/REW57809.2023.00019](https://doi.org/10.1109/REW57809.2023.00019).
[^2]: Hasso, Hussein, et al. "Abbreviation-expansion pair detection for glossary term extraction." International Working Conference on Requirements Engineering: Foundation for Software Quality. Cham: Springer International Publishing, 2022.