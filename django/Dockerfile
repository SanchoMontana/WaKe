# Use an official Python image as a base
FROM python:3.9-slim

# Set the working directory to /app
WORKDIR /app

# Copy the requirements file
COPY requirements.txt .

# Install Python dependencies
RUN apt-get update && apt-get install -y apt-utils python3-venv && rm -rf /var/lib/apt/lists/*

# Create and activate a virtual environment
RUN python -m venv /app/venv
ENV PATH="/app/venv/bin:$PATH"
RUN pip install --upgrade pip

# Activate the virtual environment and install dependencies
RUN /bin/sh -c ". /app/venv/bin/activate && pip install -r requirements.txt"

# Copy the application code
COPY . .

# Expose the port
EXPOSE 8000

# Run the command to start the development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]