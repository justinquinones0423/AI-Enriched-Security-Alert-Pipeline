# AI-Enriched-Security-Alert-Pipeline

#### A scalable data pipeline that automates the ingestion, classification, and enrichment of security logs using n8n, Airtable, and Hugging Face.

### This project demonstrates a production-style data pipeline. Unlike a simple trigger-response system, this workflow monitors a database for "unprocessed" security alerts, runs them through an AI sentiment analysis model, and writes the results back to the database while marking the record as "complete" .

#### It is worth noting that the Airtable base was designed to act as a lightweight Security Information and Event Management (SIEM) tool with the following fields:
- Alert ID
- Timestamp
- Source
- Severity
- Description
- Sentiment
- Confidence
- Processed


#### The n8n workflow design screenshot shows off the automation process which includes:
- The manual trigger, then the airtable search which queries the database for records.
- Then it follows with the data preparation where it formats the record ID and description for API compatibility.
- After comes the AI analysis in that it calls the "distilbert-base-uncased model" to evaluate the threat sentiment.
- Result formatting, the extraction of the sentiment label and confidence score.
- Database in airtable being updated, the AI Writes the AI results back into the specific Airtable record. It also flips the 'Processed' checkbox to true to prevent duplicate processing.


#### As seen in screenshots Airtable With AI-Enriched Data Parts 1 and 2, I processed over 10 diverse security scenarios, including:
- Critical threats such as ransomware signatures and potential data exfiltration.
- Warnings like locked outbound connections to suspicious IPs.
- Routine Logs that includes successful scheduled backups and security patch applications.
   
