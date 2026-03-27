Lead Sniper — GitHub Star Tracker
An automated workflow that detects high-value leads when they star a GitHub repository.

What It Does

Monitors new stargazers on a GitHub repo every 15 minutes
Fetches the user's full GitHub profile
Filters users with more than 100 followers OR 50+ public repos
Uses Groq AI to generate a personalized sales pitch
Sends an alert to Slack with the user's info and pitch

Tools Used

n8n — workflow automation
GitHub API — stargazer monitoring
Groq API (model: openai/gpt-oss-120b) — AI sales pitch generation
Slack Webhooks — notifications

How to Run

Install n8n with sudo npm install -g n8n
Run n8n start and open http://localhost:5678
Import the lead_sniper_workflow.json file
Execute the workflow

Filter Logic
A lead is high-value if:

Followers > 100 (influential person)
OR Public Repos > 50 (active developer)

Files

lead_sniper_workflow.json — import this into n8n
logic_log.md — explains rate limit handling
screenshots/ — successful Slack message and workflow execution screenshots
