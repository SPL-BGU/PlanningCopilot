<h1 align="center">Toward PDDL Planning Copilot</h2>
<p align="center">
<a href="https://glama.ai/mcp/servers/SPL-BGU/planning-copilot">
<img alt="Glama MCP Server" src="https://img.shields.io/badge/Glama-MCP%20Server-blue">
</a>
<a href="https://arxiv.org/abs/2509.12987">
<img alt="arXiv Paper" src="https://img.shields.io/badge/arXiv-2509.12987-B31B1B.svg">
</a>
<a href="https://www.python.org/downloads/release/python-31012/"><img alt="Python Version" src="https://img.shields.io/badge/python-3.10-blue"></a>
<a href="https://github.com/psf/black"><img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
</p>

# Getting Started

We present the Planning Copilot, a chatbot that brings together multiple planning tools and lets users run them using natural language instructions. It’s built on the Model Context Protocol (MCP), which makes it easy for language models to interact with external tools and systems.

The Planning Copilot is modular, so each part can be swapped out, upgraded, or extended without affecting the rest of the system. In the current implementation, Solve uses FastDownward for classical planning and Metric-FF for numeric planning, Verify uses VAL to validate plans, and Execute relies on PDDL_Plus_Parser to simulate and track plan execution.

## Dependencies
1. Make sure that Python 3.10 is installed and active (via [virtual environment](https://packaging.python.org/en/latest/guides/installing-using-pip-and-virtual-environments/#creating-a-virtual-environment) or conda environment).
2. Install the latest version of [Ollama](https://ollama.com/) to run it locally. 
3. Install all project requirements:
```
python -m pip install -r requirements.txt
```

# Usage

## How to use the environment:
1. Update all the paths and settings in the config.py file.
2. Run the LLM chat with:
```
python app.py
```
3. To change the LLM, edit the llm_with_tools.py file.
4. To add new tools, modify the MCP server in solvers_server.py.

# Citations

If you find our work interesting or the repo useful, please consider citing [this paper](https://arxiv.org/abs/2509.12987):
```
@article{benyamin2025toward,
  title={Toward PDDL Planning Copilot},
  author={Benyamin, Yarin and Mordoch, Argaman and Shperberg, Shahaf S and Stern, Roni},
  journal={arXiv preprint arXiv:2509.12987},
  year={2025}
}
```

## Hosted deployment

A hosted deployment is available on [Fronteir AI](https://fronteir.ai/mcp/spl-bgu-planningcopilot).

