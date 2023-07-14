---
name: Multimodal Recommandation System
tools: [PyTorch, FastAPI, Azure, Deep_Q_Network, Uvicorn]
image: ../assets/img/portfolio/news_recommandation_system/interface.png
description: Implementation of a real-time mutlimodal recommandation system with online reinforcement learning.
---

# Real-time news recommendation system with online reinforcement learning.

Implementation of a real-time news recommendation system with online reinforcement learning.

Articles are collected automatically with an Azure routine from Twitter, Reddit and various news APIs. They are then stored in an Azure Cosmos database for. News that is too old and no longer interesting to users is automatically deleted.

The model is a Deep Q Network. The model learns users' tastes according to two metrics. The average reward per episode (number of clicks on the recommended articles) and Jaccard's similarity to check if the model recommends news in accordance with the user's tastes according to his history.

The API for calling the model via the GUI works with FastAPI.

## Used Software and Libraries
- Programming languages: Python, Javascript
- Libraries: FastAPI, Uvicorn, PyTorch, Azure Cosmos & Automation
- Source control: GitHub