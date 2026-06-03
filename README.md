# SearxNG Self-Hosted Search Engine

## Overview

This project demonstrates the deployment of a self-hosted SearxNG instance using Docker on Windows.

SearxNG is an open-source privacy-focused metasearch engine that aggregates search results from multiple search providers into a single interface.

Unlike traditional search engines, SearxNG does not maintain its own search index. Instead, it queries multiple search providers and combines the results.

---

## Features

* Self-hosted deployment
* Docker-based setup
* Privacy-focused search
* Aggregated search results
* JSON API support
* Easily extensible for AI and RAG applications

---

## How SearxNG Works

```text
User Query
     │
     ▼
  SearxNG
     │
 ┌───┼───────────┐
 ▼   ▼           ▼
Google Bing    Brave
     │
     ▼
Merged Results
     │
     ▼
 User
```

SearxNG acts as a metasearch engine.

Instead of maintaining its own search database, it sends requests to multiple search engines and combines the results into a unified response.

---

## Project Structure

```text
.
├── core-config
├── searxng
├── docker-compose.yml
├── .env.example
├── README.md
└── docs
```

---

## Prerequisites

* Docker Desktop
* Windows 10/11
* Internet Connection

---

## Installation

Clone the repository:

```bash
git clone https://github.com/<username>/searxng-self-hosted.git

cd searxng-self-hosted
```

Create environment file:

```bash
cp .env.example .env
```

Start services:

```bash
docker compose up -d
```

Verify running containers:

```bash
docker ps
```

Open in browser:

```text
http://localhost:8080
```

---

## API Usage

Search using JSON API:

```text
http://localhost:8080/search?q=python+developer&format=json
```

Example:

```bash
curl "http://localhost:8080/search?q=machine+learning&format=json"
```

---

## Future Enhancements

* AI-powered job search agent
* LLM integration using Ollama
* Resume matching
* Job recommendation system
* RAG-based search assistant

---

## License

MIT License
