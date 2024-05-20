# Q*-Enhanced Learning

## Overview
This repository contains the implementation and experimental setup for the Q*-Enhanced Learning Algorithm, which integrates Q-Learning and A* search to optimize training processes for large language models (LLMs) using nanoGPT. This innovative approach aims to enhance efficiency and adaptability in complex training environments.

### Project Lead
- **Parag Ghorpade**
- Northeastern University

### Abstract
The Q*-Enhanced Learning project investigates a novel algorithm that combines the robust decision-making capabilities of Q-learning with the efficient path optimization of A* search. The primary goal is to improve the training efficiency and effectiveness of large language models like GPT-2, focusing on reducing computational costs and improving adaptability in complex tasks.

## nanoGPT Integration
This project utilizes [nanoGPT](https://github.com/karpathy/nanoGPT), a minimal and fast repository for training medium-sized GPTs. It serves as the base for implementing and testing our Q* algorithm. nanoGPT is based on a rewrite of [minGPT](https://github.com/karpathy/minGPT) and is designed to be simple and hackable for various needs.

![nanoGPT](assets/nanogpt.jpg)

## Installation

Dependencies include PyTorch, numpy, and several other libraries for processing and training:

```bash
pip install torch numpy transformers datasets tiktoken wandb tqdm
```

## Experimental Setup with nanoGPT
Before integrating the Q* algorithm, it is essential to establish baseline performance using nanoGPT alone. Training can be conducted on various datasets, including the provided Shakespeare character-level dataset as a quick start.

### Baseline Training
Train a baseline GPT model using the configurations provided by nanoGPT:

```bash
python train.py config/train_shakespeare_char.py
```

### Evaluate Baseline
After training, evaluate the baseline model to establish performance metrics:

```bash
python sample.py --out_dir=out-shakespeare-char
```

## Q* Algorithm Integration
Integrate the Q* algorithm into the nanoGPT training loop, modifying the `train.py` script to include the Q-learning and A* search enhancements:

### Q* Training Command
```bash
python train.py config/train_q_star.py
```

### Evaluation of Q* Model
```bash
python sample.py --out_dir=out-q-star-model
```

## Dataset Selection for Q* Testing
We will test the Q* algorithm across several key datasets to validate the enhancement:
1. **WikiText-103**
2. **BookCorpus**
3. **OpenWebText**
4. **Penn Treebank (PTB)**
5. **Common Crawl News**

## Contributions and Contact
Contributions to this project are welcome. Please feel free to fork the repository, make improvements, and submit pull requests.

For questions or further information, please contact:
- **Parag Ghorpade**
- Email: [ghorpade.p@northeastern.edu](mailto:ghorpade.p@northeastern.edu)

## Acknowledgements
This project utilizes resources from the [nanoGPT](https://github.com/karpathy/nanoGPT) repository and is conducted with support from Northeastern University.