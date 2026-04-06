# StructGen

StructGen is an innovative AI-powered tool designed for the generation and analysis of crystal structures in materials science. By leveraging advanced machine learning models, specifically a pre-trained CrystalLM language model, it enables researchers and engineers to generate novel crystal structures efficiently. The tool integrates seamlessly with CHGNet for structure relaxation and optimization, ensuring physically realistic outputs. Additionally, it employs Monte Carlo Tree Search (MCTS) to enhance the quality and diversity of generated structures, making it a comprehensive solution for crystal design and discovery.

Crystal structure prediction is a critical challenge in materials science, with applications in drug discovery, battery technology, and advanced materials development. Crystal-Gen addresses this by providing an accessible, user-friendly interface for exploring the vast space of possible crystal configurations, accelerating the discovery of new materials with desired properties.

## Features

- Generate crystal structures using a fine-tuned language model (CrystalLM)
- Visualize generated structures in 3D
- Relax and optimize crystal structures using CHGNet calculator
- Monte Carlo Tree Search (MCTS) for improved generation
- Streamlit-based web interface for easy interaction

## Installation

1. Clone or download this repository.
2. Ensure you have Python 3.8 or higher installed.
3. Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

1. Run the Streamlit application:

```bash
streamlit run app.py
```

2. Open your web browser and navigate to the provided URL (usually `http://localhost:8501`).

3. Use the interface to generate crystal structures by providing prompts or parameters.

## Project Structure

```
StructGen/
├── app.py                          # Main Streamlit application interface
├── CIFTokensier.py                 # CIF tokenizer for processing crystal data
├── mcts.py                         # Monte Carlo Tree Search implementation
├── metrics.py                      # Evaluation metrics for crystal structures
├── model_utils.py                  # Model utilities and GPT configuration
├── scorer.py                       # Physical scorer for evaluating crystal quality
├── spacegroups.txt                 # Space group data for crystallography
├── requirements.txt                # Python dependencies
├── LICENSE                         # Project license
├── README.md                       # This file
├── models/
│   └── crystallm_200m/             # Pre-trained CrystalLM model directory
│       ├── ckpt.pt                 # Model checkpoint
│       ├── config.json             # Model configuration
│       ├── merges.txt              # Tokenizer merges
│       ├── tokenizer_config.json   # Tokenizer configuration
│       └── vocab.json              # Vocabulary file
└── __pycache__/                    # Python bytecode cache (auto-generated)
```

## Requirements

- Python 3.8+
- PyTorch 2.2.0+
- ASE 3.23.0+
- CHGNet 0.4.2
- Streamlit 1.30.0+
- Other dependencies as listed in `requirements.txt`

## License

This project is licensed under the terms specified in the LICENSE file.

## Contributing

Contributions are welcome! Please feel free to submit issues or pull requests.

## Acknowledgments

- CrystalLM model for crystal structure generation
- CHGNet for structure relaxation
- ASE and PyMatGen for materials science tools
