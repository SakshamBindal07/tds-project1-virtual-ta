# 🧑‍🏫 Virtual TA – Tools in Data Science Project

This repository contains the implementation of a **Virtual Teaching Assistant (TA)** that can automatically respond to student questions based on course content and forum discussions.

## 🚀 Project Overview

As part of the IIT Madras **Tools in Data Science** course, this project aims to:

- Build a **web API** that takes a student's question (with optional image) and returns a relevant response.
- The assistant answers based on:
  - [TDS course content](https://tds.s-anand.net/) as of 15 Apr 2025
  - [Discourse forum posts](https://discourse.onlinedegree.iitm.ac.in/c/courses/tds-kb/34) from 1 Jan to 14 Apr 2025

## 📌 Features

- Accepts questions and base64-encoded images via `POST /api/`
- Returns:
  - A JSON object with `answer` and optionally `links`
  - Referenced Discourse links if relevant
- Deployed using Vercel (or any other public platform)
- Includes scraping logic and evaluation scripts

## 🛠️ Technologies Used

- Python + Flask API
- OpenAI API (GPT-4o Mini)
- Render for deployment
- Prompt engineering based on student queries
- Optional: Discourse scraping using BeautifulSoup

## 🚀 API Specification

**Endpoint:** `POST /api/`
**Request Body:** JSON containing the `question` and optional `image`
**Response:** JSON containing `answer` and optional `links` with URLs and text

## Live Demo

[TDS Virtual TA on Render](https://tds-project1-virtual-ta-hbpl.onrender.com/docs)

## Note
The knowledge_base.db file (Database file which contains all the scraped data for the project) is automatically downloaded from Google Drive during deployment.

## 🧾 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
