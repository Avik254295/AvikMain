# Use an official Python runtime as a base image
FROM python:3.9

# Set the working directory
WORKDIR /app

# Install Git
RUN apt-get update && apt-get install -y git

# Clone the repository from GitHub (Replace with your repo URL)
RUN git clone https://github.com/Avik254295/AvikMain.git /app

# Navigate to the cloned repo
WORKDIR /app

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port Cloud Run will use
ENV PORT=8080
EXPOSE 8080

# Command to run the application
CMD ["python", "server.py"]
