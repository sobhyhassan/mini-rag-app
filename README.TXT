mini-rag-app
=============

A minimal FastAPI-based RAG (Retrieval-Augmented Generation) app scaffold.

This repository includes the required Python dependencies and an example environment file. Use these steps to install, configure, and run the application.

Steps
-----

1. Create a Python virtual environment
   - python3 -m venv .venv
   - source .venv/bin/activate

2. Install dependencies
   - pip install -r requirements.txt

3. Create the environment configuration
   - copy .env.example to .env
   - set your OpenAI API key in .env:
     OPENAI_API_KEY="your_openai_api_key_here"

4. Add or verify your FastAPI app entrypoint
   - This repo currently provides the dependency and config files.
   - Ensure your FastAPI application is available in a Python file such as `main.py`, `app.py`, or similar.
   - Typical FastAPI app structure:
     ```python
     from fastapi import FastAPI
     app = FastAPI()

     @app.get('/')
     def read_root():
         return {'message': 'Hello from mini-rag'}
     ```

5. Run the app with Uvicorn
   - uvicorn main:app --reload --host 0.0.0.0 --port 8000
   - Replace `main:app` with your actual module and app object if needed.

6. Open the application
   - Visit http://localhost:8000 in your browser.

Notes
-----

- `requirements.txt` installs:
  - `fastapi`
  - `uvicorn`
  - `python-multipart`
- `assets/` is included for static or supporting files.
- Customize the README once your application code is added and the endpoint names are finalized.
