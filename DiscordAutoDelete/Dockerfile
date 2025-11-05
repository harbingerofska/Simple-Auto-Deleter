FROM python:3.11-slim

WORKDIR /app

# Copy all files from repository
COPY . .

# Install dependencies using pyproject.toml
RUN pip install --no-cache-dir -e .[speed]

# Create data directory for SQLite database
RUN mkdir -p /app/data

# Start the bot
CMD ["python", "-m", "discord_autodelete"]
