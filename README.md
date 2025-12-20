# Personal AI Assistant

A powerful command-line AI assistant powered by OpenRouter API, designed to streamline everyday tasks with intelligent automation. Features three core capabilities: professional email generation, text summarization, and creative writing prompt creation.

## Description

This Personal AI Assistant is a Python-based command-line tool that leverages the OpenRouter API to provide intelligent assistance for common writing and content tasks. Built with simplicity and efficiency in mind, it offers an interactive menu-driven interface that makes AI-powered assistance accessible to everyone.

## Features

### 1. **Email Generator**
Creates professional, well-structured emails based on your requirements. Simply provide:
- What you need to say (content)
- Who the recipient is (e.g., "my boss", "a client")
- The desired tone (e.g., "formal", "friendly", "urgent")

The assistant generates a complete email with subject line, appropriate greeting, well-structured body, and professional closing.

### 2. **Text Summarizer**
Generates concise, clear summaries of long texts. Perfect for:
- Condensing lengthy articles or documents
- Creating executive summaries
- Extracting key points from research papers or reports

Simply paste your text (supports multi-line input) and receive an intelligent summary that captures the essential information.

### 3. **Creative Writing Prompt Generator**
Creates inspiring and unique writing prompts tailored to your preferences. Specify:
- Genre or theme (e.g., "science fiction", "romance", "horror", "fantasy")
- Optional specific elements to include

Generates three distinct, engaging prompts designed to spark creativity and imagination.

## Requirements

- **Python 3.12+**
- **OpenRouter API key** (get yours at [https://openrouter.ai/keys](https://openrouter.ai/keys))
- **Dependencies**: Listed in `requirements.txt`

## Installation

Follow these steps to set up the Personal AI Assistant:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/vinipadilha/personal-ai-assistant.git
   ```

2. **Navigate to the project directory:**
   ```bash
   cd personal-ai-assistant
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## API Key Configuration

You need an OpenRouter API key to use this assistant. Choose one of the following methods:

### Option 1: Environment Variable (Recommended)

**Linux/Mac:**
```bash
export OPENROUTER_API_KEY='your-key-here'
```

**Windows (Command Prompt):**
```cmd
set OPENROUTER_API_KEY=your-key-here
```

**Windows (PowerShell):**
```powershell
$env:OPENROUTER_API_KEY='your-key-here'
```

### Option 2: Command Line Argument

Pass your API key directly when running the script:
```bash
python assistant.py your-key-here
```

**Note:** The environment variable method is recommended for security and convenience.

## Usage

To start the assistant, simply run:

```bash
python assistant.py
```

### Navigation

Once launched, you'll see an interactive menu with four options:

```
==================================================
MAIN MENU
==================================================
1. Email Generator
2. Text Summarizer
3. Creative Writing Prompt Generator
4. Exit
==================================================
```

- **Select an option** by entering a number (1-4) and pressing Enter
- **Complete the prompts** for your chosen feature
- **Review the AI-generated output**
- **Press Enter** to return to the main menu
- **Select option 4** to exit the assistant

The interface is intuitive and guides you through each step with clear prompts and instructions.

## Example Usage

### Email Generator

**Sample Input:**
```
Describe what you need to say in the email: Request a meeting to discuss Q4 budget
Who is the recipient? (e.g., 'my boss', 'a client'): my manager
What tone? (e.g., 'formal', 'friendly', 'urgent'): professional
```

**Expected Output:**
A complete professional email with:
- Subject line (e.g., "Subject: Request for Q4 Budget Discussion Meeting")
- Appropriate greeting
- Well-structured body explaining the meeting request
- Professional closing with signature placeholder

---

### Text Summarizer

**Sample Input:**
```
Paste your text (press Enter twice to finish):
Artificial intelligence has transformed the way we work and live. From 
virtual assistants to autonomous vehicles, AI technologies are becoming 
increasingly integrated into our daily routines. Machine learning algorithms 
can now process vast amounts of data to identify patterns and make predictions 
with remarkable accuracy...
[Press Enter twice]
```

**Expected Output:**
A concise summary highlighting:
- Main topic (AI transformation)
- Key examples (virtual assistants, autonomous vehicles)
- Core capabilities (pattern recognition, predictions)
- Overall impact on daily life

---

### Creative Writing Prompt Generator

**Sample Input:**
```
What genre/theme do you want? (e.g., 'science fiction', 'romance', 'horror', 'fantasy'): science fiction
Any specific element you want to include? (press Enter to skip): time travel
```

**Expected Output:**
Three unique, engaging writing prompts such as:
1. A scientist discovers time travel but can only move forward, never backward...
2. In a future where time travel is regulated by government, a rebel group...
3. A time traveler accidentally creates a paradox that threatens to erase...

Each prompt is designed to be inspiring and spark creative storytelling.

## Project Structure

```
personal-ai-assistant/
│
├── assistant.py          # Main application file
├── requirements.txt      # Python dependencies
└── README.md            # Project documentation
```

### File Descriptions

- **`assistant.py`**: Core application containing the `PersonalAssistant` class with all features and the interactive menu system
- **`requirements.txt`**: Lists all Python package dependencies (currently only `openai==1.54.0`)
- **`README.md`**: Comprehensive documentation (this file)

## Technical Details

### Architecture

The assistant is built around the `PersonalAssistant` class, which includes:

- **`__init__()`**: Initializes the OpenAI client configured for OpenRouter
- **`call_api()`**: Handles all API communications with error handling
- **`draft_email()`**: Email generation feature
- **`summarize_text()`**: Text summarization feature
- **`generate_writing_prompt()`**: Creative prompt generation feature
- **`run()`**: Main menu loop and navigation system

### AI Model

Uses **OpenAI GPT-4o-mini** via OpenRouter for:
- Fast response times
- Cost-effective operation
- High-quality output across all features

## Error Handling

The assistant includes robust error handling:
- API key validation before startup
- Exception handling for API calls
- Input validation for text summarizer
- Clear error messages with troubleshooting guidance

## Contributing

Contributions are welcome! Feel free to:
- Report bugs
- Suggest new features
- Submit pull requests
- Improve documentation



## Support

For issues, questions, or suggestions:
- Open an issue on GitHub

## Acknowledgments

- Built with [OpenRouter](https://openrouter.ai/) API
- Powered by OpenAI GPT-4o-mini model
- Uses the official OpenAI Python SDK

---

**Happy Assisting! 🤖✨**

