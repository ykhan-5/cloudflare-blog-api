# Cloudflare Blog API

For another project I'm working on I wanted a way to access blogs through their RSS feed. To do this and learn Cloudflare Workers at the same time, I built this API which allows you to fetch recent blog posts from Cloudflare's blog using their RSS feed. It supports filtering by category and limiting the number of posts returned. The API is built using Cloudflare Workers and an XML parser to dynamically fetch and process the RSS feed.

---

## Features

- **Fetch Blog Posts by Category**: Retrieve blog posts from specific categories like `AI`, `Security`, `Zero Trust`, etc.
- **Limit Results**: Specify the number of posts you want to retrieve.
- **Lightweight and Fast**: Built on Cloudflare Workers for low-latency responses.

---

## Valid Categories

The API supports the following categories:

| Category              | URL Format                     |
|-----------------------|--------------------------------|
| Policy & Legal        | `/policy-legal`               |
| Security              | `/security`                   |
| Radar                 | `/radar`                      |
| Partners              | `/partners`                   |
| Speed & Reliability   | `/speed-reliability`          |
| Product News          | `/product-news`               |
| Life at Cloudflare    | `/life-at-cloudflare`         |
| Zero Trust            | `/zero-trust`                 |
| Developers            | `/developers`                 |
| AI                    | `/ai`                         |

---

## API Endpoint

The base URL for the API is:
https://cloudflare-blog-api.ykhan5.workers.dev


---

## Request Structure

To fetch blog posts, make a `GET` request to the API with the following structure:

https://cloudflare-blog-api.ykhan5.workers.dev/category/number-of-posts


- `<category>`: The category of blog posts you want to fetch (e.g., `security`, `ai`).
- `<number-of-posts>`: The number of recent posts you want to retrieve (optional). If not provided, all posts for the category will be returned.

---
