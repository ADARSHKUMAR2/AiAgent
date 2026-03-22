🕵️‍♂️ Adarsh: The Autonomous Manor Butler
Alfred is a local AI agent built with smolagents, powered by Llama 3 (via Ollama). He is designed to handle complex tasks by writing and executing Python code on the fly, searching the web, and providing a sleek user interface via Gradio.

🚀 Features
Local-First: Runs entirely on your machine using Ollama—no expensive API tokens required for the brain.

Autonomous Reasoning: Uses a CodeAgent to write Python scripts to solve multi-step problems.

Real-time Web Search: Equipped with DuckDuckGoSearchTool to fetch live data (weather, news, music).

Gradio UI: A clean, ChatGPT-like web interface for seamless interaction.

Memory Enabled: Alfred remembers the context of your conversation across multiple turns.

🛠️ Installation
1. Clone the repository
Bash

git clone https://github.com/YOUR_USERNAME/alfred-agent.git
cd alfred-agent
2. Set up a Virtual Environment
Bash

python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
3. Install Dependencies
Bash

pip install -r requirements.txt
4. Setup Ollama
Ensure you have Ollama installed and the Llama 3 model pulled:

Bash

ollama pull llama3
🖥️ Usage
Run the main script to launch the Gradio interface:

Bash

python app.py
Then open http://127.0.0.1:7860 in your browser.

⚙️ Configuration
The agent is configured with an expanded context window to handle long search results:

Python

model = LiteLLMModel(
    model_id="ollama/llama3",
    options={"num_ctx": 8192}
)
