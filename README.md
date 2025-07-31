# Solace Agent Mesh (SAM) Evaluation Framework

This repository contains a comprehensive evaluation framework for the Solace Agent Mesh (SAM). The primary focus of this framework is to evaluate the behavior of agents. It also provides tools for benchmarking Large Language Models (LLMs) within the SAM ecosystem.

## Features

Our evaluation framework offers two primary capabilities:

### 1. Agent Evaluation
This feature allows you to test your agents by tracing the path they take to complete a task and verifying that their final response is correct. This can be treated as a "unit test" for your agents, providing a clear pass/fail grade.

### 2. LLM Benchmarking
This feature is designed for comparing the performance of different LLMs. You can run the same set of tasks with two or more LLMs and score them based on efficiency and the quality of their responses.

## Prerequisites

The following items are required when creating your own evaluations. To simply run the included demo, you can skip this section and proceed to the **Running the Demo** tutorial below.

-   **SAM Initialization:** The Solace Agent Mesh (SAM) must be initialized (`sam init`).
-   **Broker:** A running Solace PubSub+ broker is required. The framework does not support "dev mode".
-   **REST Gateway:** The `sam-rest-gateway` plugin must be installed. You can find and install it using `sam plugin catalog`.

## Running the Demo

This section provides a tutorial for running the included demo.

### Installation

1.  **Set up your environment variables:**

    Ensure that your `.env` file is populated with all the necessary values.

3.  **Create and activate a virtual environment:**
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

4.  **Install the required packages:**
    ```bash
    pip install -r requirements.txt
    ```

5.  **Run the evaluation suite:**
    ```bash
    sam eval demo/test_suite_config.json
    ```
    This command will execute the test cases defined in `demo/test_suite_config.json` and save the results in the `results/` directory.

## Usage

To run an evaluation suite, use the following command:

```bash
sam eval <path/to/test/suite>
```

This command will execute the test cases defined in the test suite configurations and save the results in the `results/` directory.

## Templates

The `templates/` directory provides starter files to help you create your own evaluations. For more details on the structure and purpose of these files, please refer to the `templates/` folder.
