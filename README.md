# AI-Enriched-Security-Alert-Pipeline

### A scalable data pipeline that automates the ingestion, classification, and enrichment of security logs using n8n, Airtable, and Hugging Face.

### This project demonstrates a production-style data pipeline. Unlike a simple trigger-response system, this workflow monitors a database for "unprocessed" security alerts, runs them through an AI sentiment analysis model, and writes the results back to the database while marking the record as "complete" .
