FROM python:3.11-slim

# Set working directory
WORKDIR /DiscordAutoDelete

# Copy project files
COPY pyproject.toml .
COPY discord_autodelete.py .

# Install dependencies
RUN pip install --no-cache-dir -e .[speed]

# Create directory for persistent database
RUN mkdir -p /DiscordAutoDelete/data

# Run the bot

CMD ["python", "-m", "discord_autodelete"]
