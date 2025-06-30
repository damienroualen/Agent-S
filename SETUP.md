# Agent-S Setup Guide

## Prerequisites

- Python 3.12 (required for compatibility)
- OpenAI API key
- Docker (for Perplexica)

## Installation

1. **Install Python 3.12:**
   ```bash
   brew install python@3.12
   ```

2. **Create virtual environment:**
   ```bash
   /usr/local/opt/python@3.12/bin/python3.12 -m venv venv312
   ```

3. **Activate virtual environment:**
   ```bash
   source venv312/bin/activate
   ```

4. **Install the package:**
   ```bash
   pip install -e .
   ```

## Running Agent-S2

1. **Activate the virtual environment:**
   ```bash
   source venv312/bin/activate
   ```

2. **Export your OpenAI API key:**
   ```bash
   export OPENAI_API_KEY="your-openai-api-key-here"
   ```

3. **Run Agent-S2:**
   ```bash
   agent_s2 \
     --provider "openai" \
     --model "gpt-4o" \
     --grounding_model_provider "openai" \
     --grounding_model "gpt-4o"
   ```

## What Agent-S2 Does

Agent-S2 is a multimodal AI agent that can:
- Take screenshots of your screen
- Analyze them using vision models
- Execute GUI actions (clicking, typing, scrolling)
- Complete tasks based on natural language instructions

## Example Tasks
- Opening applications
- Navigating websites
- Filling out forms
- Managing files and folders

## Troubleshooting

- Make sure you have the required permissions for GUI automation
- On macOS, you may need to grant accessibility permissions
- Ensure your OpenAI API key has sufficient credits for GPT-4o usage 