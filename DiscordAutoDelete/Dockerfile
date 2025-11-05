FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Copy requirements and project config
COPY requirements.txt ./
COPY pyproject.toml ./

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy the discord_autodelete package directory
COPY discord_autodelete/ ./discord_autodelete/

# Create directory for persistent database
RUN mkdir -p /app/data

# Run the bot
CMD ["python", "-m", "discord_autodelete"]
