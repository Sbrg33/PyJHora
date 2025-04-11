FROM python:3.10-slim

RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    curl \
    libglib2.0-0 \
    libsm6 \
    libxrender1 \
    libxext6 \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /workspace
COPY . /workspace

RUN pip install --upgrade pip
RUN if [ -f "requirements.txt" ]; then pip install -r requirements.txt; fi
