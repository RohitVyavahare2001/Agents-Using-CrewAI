# AI Travel & Research Assistant

This project implements an intelligent travel planning and research system using CrewAI and large language models. It features two specialized AI agents - a researcher and a writer - working together to generate detailed travel itineraries and research reports.

## Features

- **Research Agent**: Conducts in-depth research on topics or travel destinations
- **Writer Agent**: Transforms research into well-structured, readable content
- **Web Search Integration**: Uses Serper API for real-time web searches
- **Customizable Outputs**: Generate reports and itineraries based on specific inputs

## Prerequisites

- Python 3.10 or higher
- Groq API key
- Serper API key

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd <repository-name>
```

2. Install required packages:
```bash
pip install -r requirements.txt
```

3. Create a `.env` file in the project root and add your API keys:
```
groq_api_key="your_groq_api_key"
serper_api_key="your_serper_api_key"
```

## Usage

The project includes two main notebooks:

### Research & Writer Agent
This notebook demonstrates how to use AI agents for general research and content creation:

```python
from crewai import Agent, Task, Crew
from crewai_tools import SerperDevTool

# Initialize agents and create tasks
# Run the crew to generate research reports
```

### Travel Agent
This notebook shows how to create AI-powered travel itineraries:

```python
# Example usage
result = crew_instance.kickoff(
    inputs={
        "destination": "manali",
        "days": "10"
    }
)
print(result)
```

## Project Structure

```
├── .env                    # Environment variables
├── requirements.txt        # Project dependencies
├── Research & Writer Agent.ipynb  # Research agent implementation
├── travel_agent.ipynb     # Travel planning implementation
└── README.md              # Project documentation
```

## Dependencies

- crewai
- crewai[tools]
- langchain_community
- python-dotenv

## Contributing

Feel free to submit issues, fork the repository, and create pull requests for any improvements.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- CrewAI for the agent framework
- Groq for the language model API
- Serper for the search API

## Note

Make sure to keep your API keys confidential and never commit them directly to version control.