# :microscope: Variational Proteins

This repository is made as a part of the project for the course [02460 - Advanced Machine Learning](https://kurser.dtu.dk/course/02460) at DTU Compute (Spring 2021). 

The project has been initialized using the boilerplate [`eugene/variational-proteins`](https://github.com/eugene/variational-proteins) kindly provided by our Supervisor.

## The Project 

The importance of understanding genetic variations and their impact on mutations cannot be overstated. However, the computational and statistical tools that have been developed most often focus on non-epistatic mutations and low-order interactions. To address this issue, we propose a Variational Autoencoder (VAE) model based on the study [_Deep generative models of genetic variation capture mutation effects_](https://arxiv.org/abs/1712.06527).  We explore different combinations of hyperparameters and introduce three major improvements over the basic model. We show that a latent space of size 32 is the most favorable for describing the data  and that the model benefits from appropriate weight initialization for all layers. Additionally, using a constructed [_Hyperspherical Variational Auto-Encoders_](https://arxiv.org/abs/1804.00891) (S-VAE), we determine that a hyperspherical latent space is not advantageous for protein structure representation.

## Code

The project has been developed in Python and uses the PyTorch library.

**Project Structure**:
- `misc.py` is an utily file the load easily the data set stored in the `data/` folder 
- `model_statistics.ipynb` Jupyter notebook to visualize the results store in the `models/` folder
- `run-train.ps1` PowerShell script to execute the training
- `N_VAE/` ***Variational Autoencoder**
  -  `train.py` (PS: process 1)
  -  `train_basic.py` (PS: process 2)
  -  `vae.py`
  -  `vae_basic.py`
- `S_VAE/` ***Hyperspherical Variational Autoencoder***
  -  `S_vae.py`
  -  `S_vae_basic.py`
  -  `train_s_vae.py` (PS: process 3)
  -  `train_s_vae_basic.py` (PS: process 4)

**PowerShell script**:

By running the Powershell script it is possible to specify which training file to execute and to shutdown the PC after the execution:

1. Launch Windows PowerShell
2. Execute:

```
.\run-train.ps1 -process <id> -shutdown # optional
```


#### Authors

* Stefan Petrovic, s173991
* Pietro Rampazzo, s203257
* Ewa Rusiecka, s203262
