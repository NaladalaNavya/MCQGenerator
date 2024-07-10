# MCQ Generator

## Overview

MCQ Generator is a project that generates multiple-choice questions (MCQs) using LangChain and OpenAI models. The application leverages the API of OpenAI and follows a sequential chain prompt template to ensure the generation of coherent and contextually relevant questions and answers.

## Features

- Generates MCQs based on provided topics or text inputs.
- Utilizes LangChain for prompt management.
- Employs OpenAI's powerful language models for content generation.
- Sequential chain prompt template ensures the consistency and quality of the generated questions.

## Installation

1. **Clone the Repository:**

    ```sh
    git clone https://github.com/NaladalaNavya/MCQGenerator.git
    cd mcq-generator
    ```

2. **Create a Virtual Environment:**

    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. **Install Dependencies:**

    ```sh
    pip install -r requirements.txt
    ```

## Configuration

1. **OpenAI API Key:**

    You need an API key from OpenAI to access their models. Set up your API key as an environment variable:

    ```sh
    export OPENAI_API_KEY='your-openai-api-key'
    ```

2. **LangChain Configuration:**

    Configure LangChain in MCQGenerator:

    ```python
    LANGCHAIN_CONFIG = {
        'template': 'sequential_chain',
        'prompt_settings': {
            'max_tokens': 150,
            'temperature': 0.7
        }
    }
    ```

## Usage

1. **Generating MCQs:**

    You can input a topic or text for which you want to generate MCQs. The application will then use the OpenAI model through LangChain to generate a set of questions and answers.

## Example

Here's a simple example of how to generate MCQs:

```python
from mcq_generator import generate_mcqs

topic = "Machine Learning"
mcqs = generate_mcqs(topic)

for question, options in mcqs:
    print("Q:", question)
    for i, option in enumerate(options, 1):
        print(f"{i}. {option}")
```

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License.
