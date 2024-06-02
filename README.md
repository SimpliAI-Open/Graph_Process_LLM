# Harnessing the Power of Large Language Model for Uncertainty Aware Graph Processing

## 💬 About

This project is the code used for the paper 'Harnessing the Power of Large Language Models for Uncertainty-Aware Graph Processing.' Its purpose is to calculate the uncertainty of the output results of LLMs under specific tasks, thereby estimating the confidence level of the answers provided by the LLMs.

## ✨ Introduction to each file

| File           | Function                                                     |
| -------------- | ------------------------------------------------------------ |
| alpaca.json    | This file represents the specific dataset format used during the training process of this project. |
| finetune,py    | This file is the main code used for training purposes.       |
| main.py        | This file serves as the entry point for training, which completes the training by calling finetune.py. In this file, you can configure the training parameters. |
| test.py        | This file can test the cross-entropy of the model under perturbations for specific tasks after training. |
| uncertainty.py | This file can analyze the output results of the test.py file and output the confidence score. |

## 🎉How to use

#### 1️⃣ Create environment

```conda env create -f environment.yml```

#### 2️⃣ Train

Enter the relevant training parameters in main.py and run it.

> The training code used in this project is outdated and can only be used for the training of llama1 and llama2. If you want to train other more recent models, you can consider using the open-source project at https://github.com/oobabooga/text-generation-webui.

#### 3️⃣ Test

Enter the parameters in test.py and run it.

Output Explanation: 

* The 1st column represents the ground truth, 

* the 2nd column is the output result of the top1 probability, 

* the 3rd column is the probability of the top1 output result, 

* the 4th column is the output result of the top2 probability, 

* the 5th column is the probability of the top2 output result, 

* the 6th column is the standard deviation of the top1 probability for the same issue under perturbation by the model, 

* and the 7th column is the top1 probability for each perturbation.

#### 4️⃣ Uncertainty Estimation

Enter the parameters in uncertainty.py and run it.

```
@article{qian2024harnessing,
  title={Harnessing the Power of Large Language Model for Uncertainty Aware Graph Processing},
  author={Qian, Zhenyu and Qian, Yiming and Song, Yuting and Gao, Fei and Jin, Hai and Yu, Chen and Xie, Xia},
  booktitle    = {{LREC/COLING}},
  pages        = {8035--8049},
  publisher    = {{ELRA} and {ICCL}},
  year         = {2024}
}
```
