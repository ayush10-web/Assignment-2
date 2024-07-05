# Stage 1: Build stage
FROM python:3.12.4-slim AS builder

WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install -r requirements.txt

# Copy application code
COPY . .

# Stage 2: Final stage
FROM python:3.12.4-slim

WORKDIR /app

# Copy installed Python packages from builder stage
COPY --from=builder /usr/local/lib/python3.12/site-packages /usr/local/lib/python3.12/site-packages

# Copy application code from builder stage
COPY --from=builder /app .

# Expose port 3000
EXPOSE 3000

# Set environment variables if needed
ENV PYTHONUNBUFFERED=1

# Run the application
CMD ["python", "app.py"]
