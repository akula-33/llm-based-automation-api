# LLM-Based Automation API

This is an automation API built using FastAPI, designed to perform various tasks such as formatting files, counting specific dates, sorting contacts, extracting information using LLMs, and more.

---

## Features

- Install dependencies and run data generation scripts.
- Format files using Prettier.
- Count Wednesdays in a given dates file.
- Sort contacts from a JSON file.
- Write the first line of the 10 most recent log files.
- Create an index of H1 titles from Markdown files.
- Extract sender's email using LLM.
- Extract credit card numbers from images.
- Find the most similar pair of comments.
- Calculate total sales for "Gold" ticket type.

---

## Endpoints

- **GET /** - Health check endpoint.
- **POST /run** - Executes a task based on the provided description.
- **GET /read** - Reads the contents of a file given its path.

---

## Running Locally

1. Clone the repository:

    ```bash
    git clone <repo-url>
    cd llm-based-automation-api
    ```

2. Install the required dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Start the server:

    ```bash
    uvicorn app:app --host 0.0.0.0 --port 8000
    ```

4. Access the API at:

    ```
    http://localhost:8000
    ```

---

## Running with Docker

1. Build the Docker image:

    ```bash
    docker build -t <your-dockerhub-username>/llm-based-automation-api .
    ```

2. Run the Docker container:

    ```bash
    docker run -d -p 8000:8000 <your-dockerhub-username>/llm-based-automation-api
    ```

3. Access the API at:

    ```
    http://localhost:8000
    ```

---


## API Usage

- **Health Check:**

    ```bash
    curl http://localhost:8000/
    ```

- **Run a Task:**

    ```bash
    curl -X POST "http://localhost:8000/run" -H "Content-Type: application/json" -d '{"task": "Format /data/format.md using Prettier"}'
    ```

- **Read a File:**

    ```bash
    curl "http://localhost:8000/read?path=/data/format.md"
    ```

---

## Requirements

- Python 3.x
- FastAPI
- Uvicorn
- Docker (for containerization)

---

## License

This project is licensed under the MIT License.
