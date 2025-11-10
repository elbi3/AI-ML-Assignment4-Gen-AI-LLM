# FLAN-T5 for QA prompts
## Environment Setup with Anaconda & JupyterLab

- in terminal or Anaconda Prompt:
- create environment:
```shell
conda create -n llm_lab python=3.11
conda activate llm_lab
```
- install dependencies:
```shell
pip install transformers==4.37.2 torch sentencepiece
pip install jupyterlab
```
- launch:
```shell
jupyter lab
```
- additional installs:
```shell
pip install pandas
```