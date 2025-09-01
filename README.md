# CustomerSupportWorkflow_N8N

This workflow automates customer support email handling using Gmail, AI classification, and Pinecone-powered knowledge retrieval.

📌 Features

Email Trigger (Gmail): Listens for incoming emails in the inbox.

Text Classification: Categorizes emails as Customer Support or Other.

AI Agent (OpenAI via OpenRouter): Generates friendly, emoji-enhanced replies, signing off as Mr. Helpful from Tech Haven Solutions.

Knowledge Base (Pinecone + OpenAI Embeddings): Retrieves FAQ and policy info to enrich responses.

Automated Labeling: Adds labels to processed emails for organization.

Automated Reply: Sends an AI-generated response back to the customer.

⚙️ Requirements

Gmail account (OAuth2 connected in n8n)

OpenRouter account (for GPT-4o-mini responses)

OpenAI account (for embeddings)

Pinecone account & index (for FAQ retrieval)

🚀 How It Works

A new email arrives in Gmail.

The workflow classifies the email content.

If it’s a support query, the AI Agent fetches relevant FAQ data from Pinecone.

The AI Agent drafts a polite, friendly reply.

Gmail labels the email and sends the AI-generated response back to the customer.

📝 Notes

Replies are generated only for emails classified as Customer Support.

Non-support emails are ignored (via the No Operation node).

Customize the system message in the AI Agent node to adjust tone, signature, or style.
