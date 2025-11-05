FROM python:3.11-slim

# Set working directory
WORKDIR /app

# Copy all project files
COPY . .

# Install dependencies
RUN pip install --no-cache-dir -e .[speed]

# Create directory for persistent database
RUN mkdir -p /app/data

# Run the bot
CMD ["python", "-m", "discord_autodelete"]
