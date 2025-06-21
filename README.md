# News Summary AI System

An intelligent news summarization system that uses multiple AI agents to research, analyze, and generate comprehensive news reports. This system leverages advanced AI capabilities to gather information from various sources and create tailored summaries based on user preferences.

## Features

- **Multi-Agent Intelligence**: Uses specialized AI agents for research, writing, and analysis
- **Customizable Reports**: Generate summaries tailored to specific topics and user preferences
- **Automated Research**: Intelligent gathering and synthesis of information from multiple sources
- **Professional Output**: Creates well-structured markdown reports ready for consumption

## Installation

Ensure you have Python >=3.10 <3.14 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

### Step 1: Install UV

First, if you haven't already, install uv:

```bash
pip install uv
```

### Step 2: Set up Virtual Environment

Navigate to your project directory and create a virtual environment with Python 3.11:

```bash
uv venv --python 3.11.0
```

### Step 3: Activate Virtual Environment

Activate the virtual environment:

```bash
source .venv/bin/activate
```

### Step 4: Install Dependencies

Install the project dependencies:

```bash
uv sync
```

### Step 5: Optional CrewAI Setup

(Optional) Lock the dependencies and install them by using the CLI command:
```bash
crewai install
```

### Step 6: Configure Environment Variables

Create a `.env` file in the root directory of your project to store your API keys and configuration:

```bash
touch .env
```

Open the `.env` file and add your OpenAI API key and any other required environment variables:

```bash
# OpenAI API Configuration
OPENAI_API_KEY=your_openai_api_key_here

# Optional: Set OpenAI model (default is usually gpt-3.5-turbo)
OPENAI_MODEL_NAME=gpt-4

# Optional: Other API keys if needed
# SERPER_API_KEY=your_serper_api_key_here
# BROWSERLESS_API_KEY=your_browserless_api_key_here
```

**Important**: 
- Replace `your_openai_api_key_here` with your actual OpenAI API key
- Never commit your `.env` file to version control (it should be in your `.gitignore`)
- You can get your OpenAI API key from [OpenAI Platform](https://platform.openai.com/api-keys)

## Configuration

### Environment Variables
Make sure you've configured your `.env` file as described in Step 6 above.

### Agent and Task Configuration
Customize the system behavior by modifying the configuration files:

- **Agent Configuration** (`src/news_summary/config/agents.yaml`): Define the AI agents' roles, goals, and capabilities
- **Task Configuration** (`src/news_summary/config/tasks.yaml`): Specify the tasks each agent should perform
- **User Preferences** (`knowledge/user_preference.txt`): Set your preferences for news topics and report style
- **Custom Logic** (`src/news_summary/crew.py`): Add custom tools and logic for your specific use case
- **Main Entry Point** (`src/news_summary/main.py`): Customize inputs and execution flow

## Usage

### Running the News Summary System

To start the news summarization process, run this command from the root folder:

```bash
crewai run
```

This will:
1. Initialize the AI agents with their specialized roles
2. Execute the research and analysis tasks
3. Generate a comprehensive news summary report
4. Save the output as a markdown file in the `output/` directory

### Output

The system generates detailed reports in markdown format, saved in the `output/` directory. Example outputs include:
- `Banking_report.md` - Financial sector news summaries
- `Healthcare_report.md` - Healthcare industry updates
- `Funny_report.md` - Light-hearted news content
- `report.md` - General news summaries

## System Architecture

The News Summary system consists of multiple specialized AI agents that work together:

- **Research Agent**: Gathers information from various news sources and databases
- **Analysis Agent**: Processes and analyzes the collected information
- **Writing Agent**: Creates well-structured, readable summaries and reports
- **Quality Control Agent**: Reviews and ensures the accuracy and quality of outputs

Each agent has specific roles, goals, and tools defined in the configuration files, allowing for a collaborative approach to news summarization.

## Customization

### Adding New Topics
1. Update `knowledge/user_preference.txt` with your preferred news categories
2. Modify the agent configurations to focus on specific domains
3. Adjust task parameters for different types of content

### Extending Functionality
- Add custom tools in `src/news_summary/tools/`
- Implement new agents in the configuration files
- Create specialized tasks for specific use cases

## Built With

- **CrewAI Framework**: Multi-agent orchestration and coordination
- **OpenAI GPT**: Advanced language model for content generation
- **Python 3.11+**: Core programming language
- **UV**: Modern Python package and dependency management

## Support

For questions, feedback, or contributions:
- Visit our [documentation](https://docs.crewai.com)
- Reach out to us through our [GitHub repository](https://github.com/joaomdmoura/crewai)

---

*Built with the power of AI agent collaboration for intelligent news summarization.*

