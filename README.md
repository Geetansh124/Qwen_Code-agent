# Qwen Code Agent

<div align="center">
<img src="https://img.shields.io/badge/Qwen-Code%20Agent-4f46e5?style=for-the-badge" alt="Qwen Code Agent" />
<img src="https://img.shields.io/badge/Jupyter-Notebook-f37626?style=for-the-badge&logo=jupyter&logoColor=white" alt="Jupyter" />
<img src="https://img.shields.io/badge/Focus-Code%20Agents-0ea5e9?style=for-the-badge" alt="Code agents" />
</div>

An experiment workspace for exploring Qwen-powered code-agent workflows, model training artefacts, and notebook-driven development.

## Why this repository exists

This project captures the path from a language model checkpoint to a useful coding assistant: preparing data, training or adapting a model, testing its behaviour, and packaging the result for repeatable experiments.

## Workflow

```mermaid
flowchart TD
    A[Training data] --> B[Tokenization]
    B --> C[Qwen model]
    C --> D[Agent instructions]
    D --> E[Tool-aware code tasks]
    E --> F[Evaluation + iteration]
```

## Repository contents

- Kaggle-ready training notebook(s)
- Model and router experiments
- Supporting bundle and notes for reproducible runs

## Getting started

Open `codeagent_kaggle_training.ipynb` in Kaggle or Jupyter, review the configuration cells, and run the notebook in order. Keep credentials and model tokens in environment secrets—never commit them.

```bash
pip install jupyter transformers datasets peft accelerate
jupyter notebook
```

## Responsible use

Validate generated code before execution, isolate tools with least privilege, and treat model output as untrusted until tested.

## License

See the repository files for the applicable license and dataset terms.
