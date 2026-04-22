# Financial Quant Research Agent (Demo Version)

**Notice:** This project is a **demo version** of a financial agent. It does **not** support follow-up questions or file uploads. This project relies on **Yahoo Finance** data; therefore, some uncommon or niche data points may not be retrievable. Due to current limitations of **DeepSeek-V3.2**, the accuracy for complex financial queries may be low. For instance, if asking for "Apple's ERC in 2023," the success rate for a stable output is approximately **30%** because the underlying code's variable extraction functionality can be unstable and difficult for the model to identify correctly.

## 🏗️ Three-Layer System Architecture

This system operates through a structured three-layer process to ensure professional-grade financial analysis:

1.  **Layer 1: Strategic Translation (LLM)**
    The user's natural language query is first processed by a high-level LLM (acting as a Quant Director). It translates broad research needs into professional, technically rigorous prompts and execution guidelines.
2.  **Layer 2: Code Synthesis (LLM)**
    The professional prompt from Layer 1 is fed into the second LLM layer (the Quantitative Engineer). This layer generates complete, executable Python code tailored to the specific financial research plan.
3.  **Layer 3: Local Execution & Interpretation (Sandbox + LLM)**
    The generated code is executed in a **Local Sandbox environment**. The raw output (data/statistics) is then returned to the LLM, which translates the technical results into plain, easy-to-understand language and business conclusions for the user.

## 🌟 Core Technical Features

* **Financial Robustness Patches**: Automatic handling of `yfinance` MultiIndex columns and mandatory time-zone neutralization.
* **Data Alignment Audit**: Built-in monitoring for sample attrition rates and statistical Winsorization (1% and 99%).
* **Self-Healing Sandbox**: Real-time code verification with automatic multi-retry debug mechanisms if the local execution fails.

## 🛠️ Quick Start

### 1. Environment Setup
Install the necessary dependencies:
```bash
pip install openai pandas numpy yfinance statsmodels pandas_datareader
