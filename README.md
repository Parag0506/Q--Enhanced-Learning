
# Q*-Enhanced Learning

## Overview
This repository contains the implementation and experimental setup for the Q*-Enhanced Learning Algorithm, which integrates Q-Learning and A* search to optimize training processes for large language models (LLMs). This innovative approach aims to enhance efficiency and adaptability in complex training environments.

### Project Lead
- **Parag Ghorpade**
- Northeastern University

### Abstract
The Q*-Enhanced Learning project investigates a novel algorithm that combines the robust decision-making capabilities of Q-learning with the efficient path optimization of A* search. The primary goal is to improve the training efficiency and effectiveness of large language models like GPT-2, focusing on reducing computational costs and improving adaptability in complex tasks.

## File Structure

- `data/` - Datasets directory
- `models/` - Trained models and model definitions
- `src/` - Source code for the Q* algorithm
  - `train.py` - Script to train the model
  - `test.py` - Script to test the model
  - `q_star.py` - Core implementation of the Q* algorithm
- `experiments/` - Experimental setups and configuration files
- `results/` - Results and analysis notebooks
- `README.md` - Repository documentation
- `requirements.txt` - Python dependencies

## Experimental Setup
We are testing the Q* algorithm across various scenarios using five key datasets chosen for their relevance and challenge in language modeling:

1. **WikiText-103**: Features over 100 million tokens from verified Good and Featured Wikipedia articles.
2. **BookCorpus**: A rich corpus of unabridged books for deep learning training.
3. **OpenWebText**: Texts from URLs shared in Reddit posts, mirroring the data used by OpenAI.
4. **Penn Treebank (PTB)**: Well-known for focused syntax and structure experiments in NLP.
5. **Common Crawl News**: A large and diverse dataset for scalability and robustness testing.

### Proposed Algorithm
The Q* algorithm operational details:
- **Initialization**: Begin with initializing Q-values for all state-action pairs.
- **Learning Process**: For each episode:
  - Initialize state `s`
  - Choose actions using policy derived from Q (e.g., ε-greedy)
  - Execute action, observe reward and new state
  - Integrate A* heuristic to update Q-values
  - Repeat until the state is terminal

## Requirements
- Python 3.8+
- PyTorch 1.7+
- NumPy, Pandas
- Matplotlib for visualization

To install dependencies, use the following bash commands:

```bash
pip install -r requirements.txt
```

## Running Experiments
To start training, use the following bash commands:

```bash
python src/train.py --dataset data/wikitext-103 --epochs 10
```

To evaluate the model, use the following bash commands:

```bash
python src/test.py --model models/q_star_model.pt
```

## Contributions
We welcome contributions to enhance the algorithm's efficiency, extend dataset support, or improve experimental designs. Please feel free to fork this repository and submit pull requests.

## Contact
- **Parag Ghorpade**
- Email: [ghorpade.p@northeastern.edu](mailto:ghorpade.p@northeastern.edu)
- Northeastern University, Computer Science Department