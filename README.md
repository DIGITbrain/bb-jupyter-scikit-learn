# General

## Deployment type

Docker

## Image

Based on official Python image.

## Licence

BSD-3-Clause License

## Version

0.24.1

## Description

ScikitLearn is a simple open-source and efficient tools for predictive data analysis. It provides efficient state-of-the-art algorithms, accessible to non-machine learning experts, and reusable across scientific disciplines and application fields. It also takes advantage of Python interactivity and modularity to supply fast and easy prototyping. The ScikitLearn reference architecture proposes to provide a general developer environment with integrated data management and tools that can help the development process. In this stack, we created a JupyterLab manifest with ScikitLearn integration and data management part.

# Deployment

A. General example:

```sh
docker run -d --rm \
        --name scikit-learn \
        -e JUPYTER_PASSWORD=jupyterlab \
        -p 8888:8888 \
        -v $HOME/scikit-learn/data:/scikit-learn \
        digitbrain/bb-jupyter-scikit-learn:latest
```

## Parameters

|Name|Value|Description|
|-|-|-|
|Port|`-p 8888:8888`|JupyterLab WebGUI|
|Volume|`$HOME/scikit-learn/data:/scikit-learn`|Persist scikit-learn data|
|Env|`-e JUPYTER_PASSWORD=jupyterlab`|Define JupyterLab password|

## Testing

Direct your browser at: [http://\<HOST\>:8888](http://<HOST>:8888)

Run the example notebook at `/example/scikit-learn.ipynb`.

# Authentication

The WebUIs are protected by password. The default password is "jupyterlab", which can be changed with `JUPYTER_PASSWORD` enviroment variable.

# Reference

https://scikit-learn.org/stable/user_guide.html

https://scikit-learn.org/stable/auto_examples/index.html

https://jupyterlab.readthedocs.io/en/stable/