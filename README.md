# Transformer Chatbot

An interactive AI chatbot built with Jupyter Notebook and transformer-based language models.

## Overview

`Transformer-Chatbot` demonstrates a lightweight conversational interface powered by Hugging Face models. The project is implemented entirely in `AI_Chatbot.ipynb`, combining model loading, prompt handling, response generation, and a widget-based chat UI.

## Models

The notebook provides support for two pre-trained causal language models:

- `HuggingFaceTB/SmolLM2-360M`
- `TinyLlama/TinyLlama-1.1B-Chat-v1.0`

Users can switch between these models at runtime to compare response quality and performance.

## Key Features

- Device-aware model initialization with GPU fallback to CPU
- Interactive chat interface using `ipywidgets`
- Dynamic control over generation parameters:
  - temperature
  - max tokens
  - top-p sampling
  - repetition penalty
- Conversation memory with the latest 5 user-assistant exchanges
- Response cleanup to remove prompt artifacts and preserve readability
- Benchmark comparison for response time and output quality

## Installation

1. Install Python 3.10 or later.
2. Install the project dependencies either manually or by running the notebook cell that installs them.

Dependencies include:

- `transformers`
- `accelerate`
- `bitsandbytes`
- `sentencepiece`
- `ipywidgets`
- `psutil`
- `pandas`

## Usage

1. Launch Jupyter Notebook or JupyterLab.
2. Open `AI_Chatbot.ipynb`.
3. Execute the cells in order from top to bottom.
4. Enter messages into the chat widget and send them to receive AI-generated replies.
5. Use the benchmark section to compare model performance and output quality.

## Notebook Structure

- Environment setup and dependency installation
- GPU detection and device configuration
- Model loading for SmolLM2 and TinyLlama
- System prompt definition and conversation history management
- Response generation and cleanup functions
- Widget-based UI creation and event handling
- Benchmark evaluation and results display

## Notes

- The notebook uses `device_map="auto"` when loading models, which allows automatic device placement.
- The chat memory stores only the latest 5 rounds to reduce prompt size and improve generation speed.
- The benchmark uses simple heuristics to estimate output quality and compare inference speed.

## Author

Tribhuwan Singh
