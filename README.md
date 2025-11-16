

# n8n Application Setup Guide

These are the steps to build the custom Docker Image and launch the n8n application using Docker Compose.

-----

## 🚀 STEP 1: Build the **`n8n-puppeteer`** Image

You need to build a Docker Image that supports Puppeteer for n8n to perform complex web tasks.

1.  **Navigate** to the directory containing the Dockerfile:

    ```bash
    cd n8n-puppeteer
    ```

2.  **Build the Image** and tag it as **`n8n-puppeteer`**:

    ```bash
    docker build -t n8n-puppeteer .
    ```

-----

## ⚙️ STEP 2: Start the Application with Docker Compose

Use Docker Compose to create the data Volume and run the necessary services.

1.  **Navigate** to the directory containing the `docker-compose.yml` file:

    ```bash
    cd n8n-rag-v1
    ```

2.  **Create the Volume** to persist n8n's data:

    ```bash
    docker volume create n8n_data
    ```

3.  **Start** the application in detached mode (`-d`):

    ```bash
    docker compose up -d
    ```

### ✅ Access the Application

Once the services are running, you can access n8n at the following address:

**http://localhost:5678**