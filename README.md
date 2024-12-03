# LLM Voting Repository

This GitHub repository hosts the source code and data for the research paper titled "LLM Voting: Human Choices and AI Collective Decision Making," which investigates the voting behaviors of Large Language Models (LLMs), specifically GPT-4 and LLaMA-2. The paper has been accepted for publication at the AAAI Conference on AI, Ethics, and Society (AIES) and is available on arXiv: [Read the paper](https://arxiv.org/abs/2402.01766).

## Abstract
This paper investigates the voting behaviors of Large Language Models (LLMs), specifically GPT-4 and LLaMA-2, their biases, and how they align with human voting patterns. Our methodology involved using a dataset from a human voting experiment to establish a baseline for human preferences and conducting a corresponding experiment with LLM agents. We observed that the choice of voting methods and the presentation order influenced LLM voting outcomes. We found that varying the persona can reduce some of these biases and enhance alignment with human choices. While the Chain-of-Thought approach did not improve prediction accuracy, it has potential for AI explainability in the voting process. We also identified a trade-off between preference diversity and alignment accuracy in LLMs, influenced by different temperature settings. Our findings indicate that LLMs may lead to less diverse collective outcomes and biased assumptions when used in voting scenarios, emphasizing the need for cautious integration of LLMs into democratic processes.

## Repository Structure
- `agent/`: Python modules for LLM interaction.
- `data/`: Datasets including lab metadata, personas, and voting results.
- `figures/`: Generated figures and graphs for analysis.
- `llm/`: API and utilities for LLM configuration and communication.
- `memory/`: Modules for handling LLM memory and state information.
- `outcome/`: Results and analysis from various voting experiments.
   - `analyse_outcome.ipynb`: Jupyter notebook for data analysis and visualization of voting outcomes.
- `scripts/`: Python scripts for running the voting experiments.
- `EULER.md`: Computational resources documentation.
- `README.md`: This file, describing the project and setup instructions.
- `requirements.txt`: List of Python dependencies.

## Quick Start
1. **Setup Environment**:
   - Create a new Python environment using Python 3.9:
     ```bash
     python -m venv env
     source env/bin/activate
     ```
   - Install the required dependencies:
     ```bash
     pip install -r requirements.txt
     ```
2. **Environment Variables**:
   - Make sure the `OPENAI_API_KEY` is defined in the `.env` file in the root directory for API access.
3. **Run the Basic Voting Script**:
   - Navigate to the `scripts` folder and run the `pb_voting_basic.py`:
     ```bash
     cd scripts
     python pb_voting_basic.py
     ```
4. **Analyze the Outcomes**:
   - To analyze the results and generate visualizations, open the `analyse_outcome.ipynb` notebook located in the `outcome/` directory:
     ```bash
     jupyter notebook analyse_outcome.ipynb
     ```
     
## Citing Our Work
If you use this repository for your research, please cite our paper:
```bibtex
@article{yang2024llmvoting,
  title={{LLM} Voting: Human Choices and {AI} Collective Decision Making},
  author={Yang, Joshua C. and Dailisan, Damian and Korecki, Marcin and Hausladen, Carina I. and Helbing, Dirk},
  volume = {7},
  ISSN = {3065-8365},
  DOI = {10.1609/aies.v7i1.31758},
  year={2024},
  month = oct,
  pages = {1696–1708},
  journal = {Proceedings of the AAAI/ACM Conference on AI,  Ethics,  and Society},
  publisher = {Association for the Advancement of Artificial Intelligence (AAAI)},
}

