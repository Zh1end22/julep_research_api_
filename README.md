# Julep Research API

A Flask-based web service that leverages the Julep AI platform to perform topic research and return results in user-specified formats. This API is designed for easy deployment on Railway and provides a simple interface for research tasks.

**Live URL**: https://julepresearchapi-production-38fe.up.railway.app/

## Overview

The Julep Research API is a lightweight Python application built with Flask, integrating the Julep AI API to create a "Research Assistant" agent. It supports:

- Creating and managing a persistent Julep agent
- Processing POST requests to research topics in various formats (e.g., summary, detailed report)
- Reliable operation with built-in error handling and logging

Hosted on Railway, this API is ideal for developers looking to integrate AI-driven research capabilities into their projects.

## Features

- **Dynamic Research**: Submit topics and formats via API calls to get tailored research outputs
- **Agent Persistence**: Stores the Julep agent ID across container restarts
- **Error Handling**: Includes logging and timeout mechanisms for reliable operation
- **Scalable Deployment**: Optimized for Railway with Gunicorn and gevent workers

## Prerequisites

- Python 3.10+
- Git
- Docker (for local testing)
- Railway account (for deployment)
- Julep API key (obtain from [Julep](https://julep.ai/))

## Workflow Diagram

![Workflow Diagram](https://i.imgur.com/wNAB3QP.png)

## API Reference

This API allows you to:
- Create a "Research Assistant" agent powered by Julep AI
- Send requests to research any topic in your preferred format
- Check if the app is running with a health check
- Run it locally or deploy it online with minimal effort

## Getting Started

### Environment Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/julep-research-api.git
   cd julep-research-api
   ```

2. Create a `.env` file in the project root:
   ```bash
   JULEP_API_KEY=your_julep_api_key_here
   JULEP_ENVIRONMENT=production
   ```

3. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

### Local Development

Run the application directly:
```bash
python app.py
```

### Docker Deployment

1. Build the Docker image:
   ```bash
   docker build -t julep-research-api .
   ```

2. Run the container:
   ```bash
   docker run -p 5000:5000 -e JULEP_API_KEY=your_julep_api_key_here julep-research-api
   ```

3. Access the API at [http://localhost:5000](http://localhost:5000)

### Railway Deployment

1. Connect your GitHub repository to Railway
2. Set the `JULEP_API_KEY` environment variable in Railway
3. Deploy using the Dockerfile configuration

## Sample Image

![image](https://github.com/user-attachments/assets/b630b947-77b2-4236-a187-99a7968f2eca)
