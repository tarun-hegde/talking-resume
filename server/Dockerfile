# Dockerfile for server
FROM python:3.9

# Set working directory
WORKDIR /app


# Copy requirements.txt and install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy the rest of the application code
COPY . .

# Expose the port the app runs on
EXPOSE 8000

# Start the application with reload
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8000", "--reload"]