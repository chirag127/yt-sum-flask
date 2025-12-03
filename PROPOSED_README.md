# YT-Summly: AI-Powered Video Transcript Summarizer API

![Build Status](https://img.shields.io/github/actions/workflow/status/chirag127/YT-Summly-AI-Powered-Video-Transcript-Summarizer-API/ci.yml?style=flat-square)
![Code Coverage](https://img.shields.io/codecov/c/github/chirag127/YT-Summly-AI-Powered-Video-Transcript-Summarizer-API?style=flat-square)
![Tech Stack](https://img.shields.io/badge/Python-3.10%2B%20%7C%20Flask-informational?style=flat-square)
![Lint/Format](https://img.shields.io/badge/Ruff-optimized-blue?style=flat-square)
![License](https://img.shields.io/github/license/chirag127/YT-Summly-AI-Powered-Video-Transcript-Summarizer-API?color=f9d000&style=flat-square)
![GitHub Stars](https://img.shields.io/github/stars/chirag127/YT-Summly-AI-Powered-Video-Transcript-Summarizer-API?style=flat-square)

**A highly efficient, Flask-based API service that leverages AI to generate concise summaries from YouTube video transcripts, accessible via a web interface.**

This project delivers a powerful backend solution for quickly distilling the essence of YouTube videos by processing their closed captions. It's engineered for speed, efficiency, and seamless integration.

<details>
<summary>🤖 AI Agent Directives</summary>

This repository is managed by the Apex Technical Authority, operating under the **December 2025 Edition** directives. Its core objective is to provide a Zero-Defect, High-Velocity, Future-Proof API for AI-powered video summarization.

**Primary Stack:**
*   **Language:** Python 3.10+
*   **Package Management:** uv
*   **Linting & Formatting:** Ruff
*   **Testing:** Pytest
*   **Web Framework:** Flask
*   **AI Integration:** Assumed integration with a state-of-the-art NLP model for summarization (e.g., leveraging libraries like `transformers` or a cloud-based NLP API).

**Architectural Principles:**
*   **Modular Monolith:** Adheres to a clean architecture with well-defined modules for transcript fetching, AI processing, and API exposure.
*   **SOLID Principles:** Applied rigorously to ensure maintainability and extensibility.
*   **DRY (Don't Repeat Yourself):** Code duplication is actively minimized.
*   **YAGNI (You Ain't Gonna Need It):** Features are implemented based on current requirements.

**Verification Commands:**
*   **Dependency Installation:** `uv pip install --frozen`
*   **Linting & Formatting Check:** `ruff check .`
*   **Testing:** `pytest`

**AI Model Interaction:**
*   All interactions with AI models must be robust, include proper error handling, and adhere to API rate limits and security best practices. Specific model details should be abstracted.

</details>

## 1. Table of Contents

*   [Features](#features)
*   [Architecture](#architecture)
*   [Getting Started](#getting-started)
*   [Usage](#usage)
*   [Development](#development)
*   [Contributing](#contributing)
*   [License](#license)

## 2. Features

*   **AI-Powered Summarization:** Utilizes advanced NLP techniques to generate concise summaries of video content.
*   **YouTube Transcript Fetching:** Automatically retrieves closed captions from YouTube videos.
*   **Flask API:** Exposes a robust RESTful API for programmatic access.
*   **Web Interface:** Provides a simple web UI for direct interaction and testing.
*   **High Performance:** Optimized for speed and efficient resource utilization.

## 3. Architecture

mermaid
graph TD
    A[User/Client] --> B(Web Interface);
    B --> C{Flask API Backend};
    C --> D[Transcript Fetcher];
    D --> E(YouTube API);
    C --> F[AI Summarization Service];
    F --> G(NLP Model/Library);
    C --> H[Response Handler];
    H --> B;
    H --> A;


## 4. Getting Started

### Prerequisites

*   Python 3.10+ (Managed by `uv`)
*   `git`

### Installation

1.  **Clone the repository:**
    bash
    git clone https://github.com/chirag127/YT-Summly-AI-Powered-Video-Transcript-Summarizer-API.git
    cd YT-Summly-AI-Powered-Video-Transcript-Summarizer-API
    

2.  **Set up the Python environment using `uv`:**
    bash
    uv venv
    source .venv/bin/activate
    uv pip install --frozen
    

## 5. Usage

### Running the API Server

bash
python -m flask run


The API will be accessible at `http://127.0.0.1:5000`.

### API Endpoints

*   `POST /summarize`:
    *   **Body:** `{"url": "<youtube_video_url>"}`
    *   **Response:** `{"summary": "<generated_summary>", "transcript": "<original_transcript>"}`

### Web Interface

Navigate to `http://127.0.0.1:5000` in your browser to use the interactive summarization tool.

## 6. Development

### Project Structure

bash
YT-Summly-AI-Powered-Video-Transcript-Summarizer-API/
├── app/
│   ├── __init__.py
│   ├── api.py          # API routes and request handling
│   ├── core.py         # Core summarization logic
│   ├── services.py     # External service integrations (YouTube, AI)
│   └── templates/
│       └── index.html  # Web interface template
├── tests/
│   ├── __init__.py
│   ├── test_api.py
│   └── test_core.py
├── .gitignore
├── AGENTS.md
├── badges.yml
├── CONTRIBUTING.md
├── LICENSE
├── PROPOSED_README.md
├── README.md
├── ISSUE_TEMPLATE/
│   └── bug_report.md
├── PULL_REQUEST_TEMPLATE.md
├── SECURITY.md
├── pyproject.toml
├── requirements.txt
├── .venv/
└── run.py              # Script to run the Flask app


### Development Scripts

| Script          | Description                                      |
| :-------------- | :----------------------------------------------- |
| `uv venv`       | Create virtual environment                       |
| `source .venv/bin/activate` | Activate virtual environment               |
| `uv pip install --frozen` | Install dependencies                           |
| `ruff check .`  | Lint and format code                             |
| `pytest`        | Run all tests                                    |
| `python -m flask run` | Start the development server                     |

## 7. Contributing

Contributions are welcome! Please refer to the [CONTRIBUTING.md](https://github.com/chirag127/YT-Summly-AI-Powered-Video-Transcript-Summarizer-API/blob/main/.github/CONTRIBUTING.md) file for detailed guidelines.

## 8. License

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0) license. See the [LICENSE](https://github.com/chirag127/YT-Summly-AI-Powered-Video-Transcript-Summarizer-API/blob/main/LICENSE) file for more details.

