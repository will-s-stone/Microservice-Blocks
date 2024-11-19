FROM python:3.9-slim

# Set the working directory
WORKDIR /app

# Install Poetry
RUN pip install --no-cache-dir poetry

# Copy the pyproject.toml and poetry.lock files
COPY pyproject.toml poetry.lock ./

# Install dependencies
RUN poetry install --no-root --no-dev

# Copy the application code
COPY . .

# Set the entry point
ENTRYPOINT ["python", "main.py"]