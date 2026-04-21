# llama-cpp
This project provides a plug-and-play Docker Compose environment to deploy a high-performance Llama 3.1 8B Instruct server. It automates the model download and configures the llama.cpp server with NVIDIA GPU acceleration (CUDA) out of the box.

🚀 Key Features
Automatic Model Fetching: Downloads the optimized Llama-3.1-8B-Instruct-Q5_K_M GGUF model automatically on the first run.
NVIDIA CUDA Integration: Pre-configured to utilize your GPU via the ghcr.io/ggml-org/llama.cpp:server-cuda image.
High Performance: Enabled optimizations including --flash-attn, high context size (8192), and full GPU layer offloading (-ngl 99).
OpenAI Compatible API: Serves the model on port 8080, compatible with most AI frontends and tools.
🛠️ Prerequisites
Before running, ensure you have the following installed:
Docker and Docker Compose.
NVIDIA Container Toolkit (to allow Docker to access your GPU).
Recent NVIDIA drivers installed on the host machine.

📦 Getting Started
Clone this repository:
git clone https://github.com/your-username/llama-cpp-docker.git
cd llama-cpp-docker

Start the stack:
docker compose up -d

Monitor the Download:
docker compose logs -f llamacpp-llama-cpp-1

Web address
http://localhost:8080/
