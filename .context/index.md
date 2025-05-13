---
module-name: agents-from-scratch
description: A guide to building agents from scratch, focusing on an email assistant with Gmail API integration
main-technologies:
  - Python 3.11+
  - LangGraph
  - LangChain
  - OpenAI
  - LangSmith
related-modules: []
conventions:
  - Organized into sections (agent, evaluation, HITL, memory)
  - Each section has a notebook and accompanying code
---

# Agents From Scratch

## Project Overview
This project is a guide to building agents from scratch, culminating in an "ambient" agent that can manage emails with Gmail API integration. The project is structured into four progressive sections, each building on the previous one.

## Directory Structure
- `src/email_assistant/`: Core implementation code
- `notebooks/`: Jupyter notebooks for each section
- `eval/`: Evaluation code and datasets
- `tests/`: Test suite for the email assistant

## Key Components
1. **Basic Agent**: Email triage and response system
2. **Evaluation**: Testing framework with LangSmith integration
3. **Human-in-the-Loop (HITL)**: User review capabilities
4. **Memory**: Persistent memory for learning from feedback

## Setup and Usage
- Requires Python 3.11+
- Uses virtual environment in `.venv/`
- Requires OpenAI and LangSmith API keys
- Can be installed with `pip install -e .`
- Run the LangGraph development server with `langgraph dev`
- Access the LangGraph Studio UI at https://smith.langchain.com/studio/?baseUrl=http://127.0.0.1:2024

## LangGraph Integration
This project heavily utilizes LangGraph for building agent workflows:
- Creates graph-based agents with nodes and edges
- Implements checkpoints for state management
- Supports human-in-the-loop interactions
- Provides memory capabilities for persistent learning

## Available Graphs
The following graphs are registered with the LangGraph development server:
- langgraph101: Basic LangGraph example
- email_assistant: Email triage and response system
- email_assistant_hitl: Email assistant with human-in-the-loop capabilities
- email_assistant_hitl_memory: Email assistant with HITL and memory
- email_assistant_hitl_memory_gmail: Email assistant with Gmail integration
- cron: Scheduled tasks for email processing
