# LangChain Tutorial

Welcome to the LangChain Tutorial codebase! This repository provides a hands-on, chapter-based guide to building applications with [LangChain](https://python.langchain.com/), a powerful framework for developing language model-powered workflows and agents. The tutorial is organized into chapters, each focusing on a different aspect of LangChain, from basic LLM calls to advanced agent and database integrations.

## Table of Contents
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Chapter Overview](#chapter-overview)
- [Database Example](#database-example)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

---

## Project Structure
```
Langchain_Tutorial/
│   main.py
│   pyproject.toml
│   README.md
├── CH-1/
│   ├── 1_LLM_Call.ipynb
│   ├── 2_Messages.ipynb
│   └── 3_Structured_Outputs.ipynb
├── CH-2/
│   ├── 1_first_chain.ipynb
│   ├── 2_chain_with_customRunnable.ipynb
│   ├── 3_parallel_chains.ipynb
│   └── 4_conditional_chains.ipynb
├── CH-3/
│   ├── 1_ReAct_Agent_Intro.ipynb
│   ├── 2_React_DB_Agent.ipynb
│   ├── init_db.py
│   └── SalesDB/
```

- **main.py**: Entry point for the project (prints a welcome message).
- **pyproject.toml**: Project metadata and dependencies.
- **CH-1/**: Introduction to LLM calls, message handling, and structured outputs.
- **CH-2/**: Building chains, custom runnables, parallel and conditional chains.
- **CH-3/**: Agent-based workflows and database integration.

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/yourusername/langchain-tutorial.git
   cd langchain-tutorial
   ```
2. **Create a virtual environment (recommended):**
   ```sh
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```
3. **Install dependencies:**
   ```sh
   pip install -r requirements.txt
   # Or use poetry/pip with pyproject.toml
   ```

## Usage

- **Run the main script:**
  ```sh
  python main.py
  ```
- **Explore the Jupyter notebooks:**
  Open any notebook in the `CH-1`, `CH-2`, or `CH-3` folders to follow the tutorial interactively.
- **Database Example:**
  - In `CH-3`, run `init_db.py` to set up a sample SQLite database in `SalesDB/sales.db`.

## Chapter Overview

### CH-1: Getting Started with LLMs
- `1_LLM_Call.ipynb`: Basic language model calls.
- `2_Messages.ipynb`: Working with message objects.
- `3_Structured_Outputs.ipynb`: Producing structured outputs from LLMs.

### CH-2: Building Chains
- `1_first_chain.ipynb`: Creating your first chain.
- `2_chain_with_customRunnable.ipynb`: Custom runnables in chains.
- `3_parallel_chains.ipynb`: Running chains in parallel.
- `4_conditional_chains.ipynb`: Conditional logic in chains.

### CH-3: Agents & Database Integration
- `1_ReAct_Agent_Intro.ipynb`: Introduction to ReAct agents.
- `2_React_DB_Agent.ipynb`: Using agents with a database.
- `init_db.py`: Script to initialize a sample sales database.
- `SalesDB/`: Contains the SQLite database file after initialization.

## Database Example

The `init_db.py` script in `CH-3` creates a sample `orders` table and populates it with example data:
```python
CREATE TABLE IF NOT EXISTS orders (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    customer_name TEXT NOT NULL,
    product_name TEXT NOT NULL,
    quantity INTEGER NOT NULL,
    price REAL NOT NULL,
    total REAL NOT NULL
)
```
Sample data includes orders for laptops, smartphones, and tablets. This database is used in agent demonstrations in CH-3.

## Dependencies

Key dependencies (see `pyproject.toml`):
- `langchain`
- `langchain-community`
- `langchain-core`
- `langchain-openai`
- `load-dotenv`
- `openai`
- `wikipedia`

## Contributing

Contributions are welcome! Please open issues or submit pull requests for improvements, bug fixes, or new tutorial chapters.

## License

This project is licensed under the MIT License.

---

Happy learning with LangChain!

