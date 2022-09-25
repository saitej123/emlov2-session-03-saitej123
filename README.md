<div align="center">

# Lightning-Hydra-Template with CIFAR Dataset with Optuna + tensorboard

[![python](https://img.shields.io/badge/-Python_3.7_%7C_3.8_%7C_3.9_%7C_3.10-blue?logo=python&logoColor=white)](https://github.com/pre-commit/pre-commit)
[![pytorch](https://img.shields.io/badge/PyTorch_1.8+-ee4c2c?logo=pytorch&logoColor=white)](https://pytorch.org/get-started/locally/)
[![lightning](https://img.shields.io/badge/-Lightning_1.6+-792ee5?logo=pytorchlightning&logoColor=white)](https://pytorchlightning.ai/)
[![hydra](https://img.shields.io/badge/Config-Hydra_1.2-89b8cd)](https://hydra.cc/)


<!-- <a href="https://www.python.org/"><img alt="Python" src="https://img.shields.io/badge/-Python 3.7+-blue?style=for-the-badge&logo=python&logoColor=white"></a> -->

<!-- <a href="https://pytorch.org/get-started/locally/"><img alt="PyTorch" src="https://img.shields.io/badge/-PyTorch 1.8+-ee4c2c?style=for-the-badge&logo=pytorch&logoColor=white"></a>
<a href="https://pytorchlightning.ai/"><img alt="Lightning" src="https://img.shields.io/badge/-Lightning 1.6+-792ee5?style=for-the-badge&logo=pytorchlightning&logoColor=white"></a>
<a href="https://hydra.cc/"><img alt="Config: hydra" src="https://img.shields.io/badge/config-hydra 1.2-89b8cd?style=for-the-badge&labelColor=gray"></a>
<a href="https://black.readthedocs.io/en/stable/"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-black.svg?style=for-the-badge&labelColor=gray"></a> -->
</div>

# Experiment Results

- Google drive Link for dvc - <https://drive.google.com/drive/folders/1xV0qTuvvboYnyRspw5aeMos06WOKs5Mg?usp=sharing>

- Tensorboard Link for dvc -  <https://tensorboard.dev/experiment/WuPX9JlwRvi4IPdoqlntww/#scalars>

###### *Training stopped in-between because of CPU training (with less epochs) & failed in colab instance*

Best HyperParameter from experiment

 ```
 name: optuna
 best_params:
    model.optimizer._target_: torch.optim.Adam
    model.optimizer.lr: 0.080057
    datamodule.batch_size: 8

  ```


# DVC Steps
```
dvc add data
dvc add logs
dvc push -r gdrive
```
**Link** : <https://drive.google.com/drive/folders/1xV0qTuvvboYnyRspw5aeMos06WOKs5Mg?usp=sharing>
![1](images/dvc_gcp.jpg)

# Hyper-parameter search Optuna
- Set hyper-parameters for experiment tracking
- Find the best batch_size and learning rate, and optimizer
- Optimizers have to be one of Adam, SGD, RMSProp
 ![1](images/experiment_dev.jpg)

# Tensorboard  Results

 <https://tensorboard.dev/experiment/HZTVAzfkSDC8EfVfAW99NQ/>

 ![1](images/tensor_board.jpg)
 ![2](images/tensor_2.jpg)
