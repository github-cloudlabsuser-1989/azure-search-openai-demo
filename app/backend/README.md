# Backend Module

This module contains the backend logic for our application. It is primarily written in Python and uses several libraries for asynchronous programming, data manipulation, and interaction with external services.

## Structure

The main components of the backend module are:

- `approaches`: This directory contains the implementation of different approaches for handling and processing data. The main class is `Approach`, which is an abstract base class for different approaches. Each approach must implement the `run` and `run_stream` methods.

- `core`: This directory contains core functionalities like authentication.

- `text`: This directory contains utilities for text processing.

## Key Files

- `approach.py`: This file contains the implementation of the `Approach` class and related data classes. The `Approach` class is used to define different approaches for handling and processing data.

- `authentication.py`: This file contains the `AuthenticationHelper` class which is used for building security filters based on provided overrides and authentication claims.

## Classes

- `Document`: Represents a document with its properties and metadata.

- `ThoughtStep`: Represents a thought step with its title, description, and optional properties.

- `Approach`: Abstract base class for different approaches.

## Usage

To use the backend module, you need to create an instance of the `Approach` class (or a class that inherits from it) and call its methods. For example, you can call the `search` method to perform a search operation based on the provided parameters.

## Dependencies

The backend module depends on several external libraries, including:

- `aiohttp`: For making HTTP requests.
- `azure.search.documents.aio`: For interacting with Azure Search.
- `openai`: For using OpenAI's services.

Please make sure to install these dependencies before running the application.

## Contributing

Contributions are welcome. Please make sure to follow the existing code style and add tests for any new features or changes.

## Testing

Testing is an essential part of the development process. Here's how you can run tests for the backend module:

1. **Unit Testing**: Each module in the backend should have corresponding unit tests. These tests are designed to ensure that individual functions and methods work as expected. You can run these tests using a test runner like `pytest`.

2. **Integration Testing**: These tests are designed to ensure that different parts of the backend work together correctly. They might involve testing the interaction between the `Approach`, `Document`, and `ThoughtStep` classes, for example.

3. **End-to-End Testing**: End-to-end tests are used to test the system as a whole. They simulate real user scenarios and ensure that all parts of the system work together correctly.

To run the tests, navigate to the `app/backend` directory and use the command `pytest`. This will automatically discover and run the tests. Make sure all tests pass before you commit your changes.

In addition to running tests locally, we also use Continuous Integration (CI) to automatically run tests whenever changes are pushed to the repository. This helps catch issues early and ensures the stability of the codebase.

Remember, when adding new features or making changes, it's important to also add corresponding tests. This helps ensure the continued correctness of the code.

## License

This project is licensed under the MIT License. See the LICENSE file for more details.

## Setup

Before you can run the backend module or its tests, you need to set up your environment:

1. **Clone the Repository**: Clone the repository to your local machine.

2. **Install Dependencies**: Navigate to the `app/backend` directory and install the required dependencies using pip:

pip install -r requirements.txt



3. **Set Environment Variables**: If the backend module requires any environment variables (like API keys or database URLs), make sure to set them in your environment.

## Setting Up Environment Variables

The backend module requires several environment variables to function correctly. Here's a list of the required environment variables and a brief description of each:

1. **OPENAI_API_KEY**: This is the API key for OpenAI. It's used to authenticate requests to the OpenAI API.

2. **AZURE_SEARCH_API_KEY**: This is the API key for Azure Search. It's used to authenticate requests to the Azure Search service.

3. **VISION_API_KEY**: This is the API key for the Vision service. It's used to authenticate requests to the Vision service.

4. **DATABASE_URL**: This is the connection string for your database. It should include the username, password, host, port, and database name.

5. **EMBEDDING_MODEL**: This is the name of the embedding model to use.

6. **EMBEDDING_DIMENSIONS**: This is the number of dimensions for the embedding model.

7. **QUERY_LANGUAGE**: This is the language to use for queries.

8. **QUERY_SPELLER**: This is the speller to use for queries.

9. **VISION_ENDPOINT**: This is the endpoint for the Vision service.

You can set these environment variables in your operating system, or you can use a `.env` file if you're using a tool like `python-dotenv`. Here's an example of what your `.env` file might look like:

OPENAI_API_KEY=your_openai_api_key AZURE_SEARCH_API_KEY=your_azure_search_api_key VISION_API_KEY=your_vision_api_key DATABASE_URL=your_database_url EMBEDDING_MODEL=your_embedding_model EMBEDDING_DIMENSIONS=your_embedding_dimensions QUERY_LANGUAGE=your_query_language QUERY_SPELLER=your_query_speller VISION_ENDPOINT=your_vision_endpoint


Remember to replace `your_openai_api_key`, `your_azure_search_api_key`, etc. with your actual keys and values. Also, make sure not to commit your `.env` file or any other files containing sensitive information to version control.

## Running Tests

To run the tests, navigate to the `app/backend` directory and use the command `pytest`. This will automatically discover and run the tests:

pytest


Make sure all tests pass before you commit your changes.

## Introducing Changes

When you're ready to introduce changes:

1. **Create a Branch**: Always create a new branch for your changes. This keeps the main branch stable and makes it easier to review and manage pull requests.

2. **Make Your Changes**: Make your changes to the code. Remember to follow the existing code style.

3. **Write Tests**: Write tests for your changes. This helps ensure that your changes work as expected and don't break existing functionality.

4. **Run All Tests**: Run all tests to make sure your changes didn't break anything.

5. **Commit Your Changes**: Once all tests pass, commit your changes. Make sure to write a clear and meaningful commit message.

## Pull Requests

Once you've committed your changes, you can create a pull request:

1. **Push Your Branch**: Push your branch to the repository.

2. **Create a Pull Request**: On GitHub, navigate to the main page of the repository and click on "New pull request". Select your branch from the dropdown and click "Create pull request".

3. **Describe Your Changes**: In the pull request description, describe your changes. Include any information that will help reviewers understand and test your changes.

4. **Wait for Review**: Once you've created the pull request, wait for it to be reviewed and merged. You might need to make some changes based on the feedback you receiv			e.

5. **Merge Your Changes**: Once your pull request has been approved, you can merge your changes into the main branch.
