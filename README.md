# 🧠 Functions Used in `01_hello_agent.ipynb`

This document lists and explains all the key functions used in the Hello Agent project.

---

## 1. `initialize_agent(name, instructions, tools=None, handoffs=None)`

**Description:**  
Creates and initializes an AI agent using the OpenAI SDK.

**Parameters:**
- `name` (str): Name of the agent.
- `instructions` (str): Prompt or behavioral instructions for the agent.
- `tools` (list, optional): Tools the agent can use.
- `handoffs` (list, optional): Other agents to whom this agent can hand off tasks.

**Returns:**  
An `Agent` object.

---

## 2. `run_agent(agent, input_text)`

**Description:**  
Runs a specified agent on a given user input.

**Parameters:**
- `agent` (Agent): The agent to run.
- `input_text` (str): User input text to be processed.

**Returns:**  
A `RunResult` object with the agent's response.

---

## 3. `handoff_to_agent(agent, input_text)`

**Description:**  
Passes the task to a different agent based on defined handoffs.

**Parameters:**
- `agent` (Agent): Current agent processing the input.
- `input_text` (str): The task or message to be handed over.

**Returns:**  
Response from the handoff agent.

---

## 4. `initialize_tools()`

**Description:**  
Initializes a list of tools (functions) that the agents can use.

**Returns:**  
List of available tools.

---

## 5. `setup_handoffs()`

**Description:**  
Sets up the delegation system for agents.

**Returns:**  
List of handoff-capable agents.

---

## 6. `main()`

**Description:**  
Main function to run the overall agent system. It initializes everything and processes user input.

**Returns:**  
None.

---

## ✅ SDK-Based Functions Used

Alongside custom functions, some OpenAI Agents SDK features are used:

- `Agent(...)`: Used to define a new agent.
- `@function_tool`: Decorator to convert Python functions into agent-usable tools.
- `Runner.run(...)`: Runs an agent and returns results.
- `@guardrail`: (if used) For validating inputs/outputs.
- `WebSearchTool()`: Example of a built-in tool that can be added.

---

> ✨ This file documents the core logic of your Hello Agent project for better understanding and collaboration. Happy coding!
