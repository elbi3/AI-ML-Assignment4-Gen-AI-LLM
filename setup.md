# FLAN-T5 for Gen AI (Book Review)
## Environment Setup with Anaconda & JupyterLab

- in terminal or Anaconda Prompt:
- create environment:
```shell
conda create -n llm_lab python=3.11
conda activate llm_lab
```
- install dependencies:
```shell
# pip install transformers==4.37.2 torch sentencepiece
pip install torch transformers sentencepiece jupyterlab pandas
```
- verify installs:
```shell
python -m pip show transformers torch sentencepiece
```

- launch from Anaconda Prompt:
```shell
jupyter lab
```

note:
I have trouble getting Anaconda Prompt and Jupyter Lab to sync when doing installs through Anacaonda Prompt? jupyterlab does not show as installed in the GUI even though we installed it above
- still streamlining my JupyterLab and active kernel setup, not sure what is needed here, I did all this:
```shell
conda install -c conda-forge jupyterlab //might be extra
conda install ipykernel nb_conda_kernels
python -m ipykernel install --user --name=llm_lab --display-name "LLM Lab (Flan-T5)"
```
^ registering the current environment as a Jupyter kernel always comes up
`--name=llm_lab` gives Jupyter an internal ID for the kernel
`--display-name="LLM Lab (Flan-T5)"` is what you'll see in JupyterLab's dropdown list

- other
```shell
pip install -U jupyter ipywidgets
```