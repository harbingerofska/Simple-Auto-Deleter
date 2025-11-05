FROM python:3.11-slim

WORKDIR /app

# Copy project files
COPY pyproject.toml .

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY discordautodelete

# Create directory for persistent database
RUN mkdir -p /app/data

# Run the bot
CMD ["python", "-m", "discord_autodelete"]




