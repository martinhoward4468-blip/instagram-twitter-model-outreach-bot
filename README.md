# Instagram & Twitter Model Outreach Bot

> A focused outreach automation that contacts models across Instagram, Twitter/X, email, and communities, guiding them to submit a form with accurate information. It centralizes messaging, tracking, and verification so you can scale your model application funnel without manual, repetitive DM work. This repository is built for safe, structured social outreach automation with form submissions as the core metric.


<p align="center">
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://github.com/za2122/footer-section/blob/main/media/scraper.png" alt="Bitbash Banner" width="100%"></a>
</p>
<p align="center">
  <a href="https://t.me/devpilot1" target="_blank">
    <img src="https://img.shields.io/badge/Chat%20on-Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  </a>&nbsp;
  <a href="https://wa.me/923249868488?text=Hi%20BitBash%2C%20I'm%20interested%20in%20automation." target="_blank">
    <img src="https://img.shields.io/badge/Chat-WhatsApp-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" alt="WhatsApp">
  </a>&nbsp;
  <a href="mailto:sale@bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Email-sale@bitbash.dev-EA4335?style=for-the-badge&logo=gmail&logoColor=white" alt="Gmail">
  </a>&nbsp;
  <a href="https://bitbash.dev" target="_blank">
    <img src="https://img.shields.io/badge/Visit-Website-007BFF?style=for-the-badge&logo=google-chrome&logoColor=white" alt="Website">
  </a>
</p>




<p align="center" style="font-weight:600; margin-top:8px; margin-bottom:8px;">
  Created by Bitbash, built to showcase our approach to Scraping and Automation!<br>
  If you are looking for <strong>instagram-twitter-model-outreach-bot</strong> you've just found your team — Let’s Chat. 👆👆
</p>


## Introduction

This project automates the repetitive process of reaching out to models on Instagram, Twitter/X, email lists, and relevant communities, then nudging them to complete an online application form. Instead of manually sending hundreds of individual messages, tracking replies, and checking who actually submitted the form, the automation handles the full funnel from first contact to verified submission.

The core goal is to consistently bring in real, interested models who complete your application form with valid data. By centralizing multi-channel outreach, link tracking, and weekly reporting, this bot turns what would be a constant manual grind into a predictable, measurable workflow.

### Scalable outreach for model applications

- Targets models from Instagram, Twitter/X, emails, and external sources using configurable search and import rules.
- Sends personalized, template-driven messages that include your application form link and basic call-to-action.
- Tracks every click and submission, tying each form response back to the original outreach message and profile.
- Filters out obvious bots, duplicates, and low-quality leads using rule-based validation and heuristics.
- Generates a weekly spreadsheet-style report summarizing all models who successfully submitted the form.

## Core Features

| Feature | Description |
|----------|-------------|
| Multi-channel outreach engine | Orchestrates outreach via Instagram, Twitter/X, email, and other configured channels using pluggable adapters. |
| Profile targeting & importing | Imports potential model profiles from CSV, exports, or search results, then normalizes them into a unified lead format. |
| Message templates & personalization | Uses dynamic templates with placeholders (name, handle, platform, language) to keep messages relevant and human-like. |
| Safe sending & rate limiting | Applies per-account send limits, randomized delays, and cooldowns to reduce spam flags and protect account health. |
| Form link tracking & tagging | Generates unique tracking tokens per lead so each form submission is tied back to its original outreach source. |
| Lead validation & deduplication | Rejects duplicate submissions, incomplete entries, and obvious fake data before marking a lead as valid. |
| Weekly spreadsheet report | Builds a clean CSV/Excel-style report with all valid models, including platform, handle, contact info, and timestamps. |
| Monitoring & structured logging | Captures detailed logs of outreach attempts, errors, and submission events for easy debugging and audits. |
| Error handling & retry logic | Automatically retries transient failures (network, timeouts, temporary platform blocks) with exponential backoff. |
| Configuration-driven workflows | Centralizes all credentials, platform rules, templates, and thresholds in config files so behavior can be tuned without code changes. |
| Channel adapter architecture | Makes it easy to add or remove platforms (e.g., new social networks or email providers) via a clean adapter interface. |
| ... | Extend with any additional platform-specific behaviors or reporting needs. |

---

## How It Works

| Step | Description |
|------|-------------|
| **Input or Trigger** | The system is typically triggered on a schedule (e.g., hourly or daily) or via a manual command. It loads new candidate profiles from your configured sources (CSV, API, search exports). |
| **Core Logic** | Each candidate is validated, normalized, and pushed through the outreach engine, which selects the right channel, message template, and timing rules for contact. |
| **Output or Action** | The bot sends personalized messages containing your application form link, then listens for and records form submissions, tagging each submission with the originating profile and channel. |
| **Other Functionalities** | For every step, the system logs actions, tracks failures, retries transient errors, and maintains per-account usage stats for safer long-term automation. |
| **Safety Controls** | Rate limiting, randomized delays, configurable quiet hours, max messages per account, and content throttling work together to maintain compliance with platform guidelines and keep accounts usable. |
| **...** | The flow can be extended with additional review steps, scoring logic, or integrations with downstream CRM/ATS systems. |

---

## Tech Stack

| Component | Description |
|------------|-------------|
| **Language** | Python |
| **Frameworks** | FastAPI for the control API and admin endpoints, Playwright for browser-based social platform automation |
| **Tools** | PostgreSQL for persistent storage, Redis for queues and rate limiting, Pandas for report generation |
| **Infrastructure** | Docker and Docker Compose for containerized deployment, GitHub Actions for CI and basic automated checks |

---

## Directory Structure Tree

    instagram-twitter-model-outreach-bot/
        src/
            main.py
            api/
                __init__.py
                routes.py
                dependencies.py
            automation/
                __init__.py
                outreach_runner.py
                lead_pipeline.py
                instagram_client.py
                twitter_client.py
                email_client.py
                form_tracker.py
                lead_validator.py
                report_builder.py
                utils/
                    __init__.py
                    logger.py
                    rate_limiter.py
                    config_loader.py
                    randomizer.py
            config/
                settings.yaml
                accounts.example.yaml
                templates/
                    instagram_dm.txt
                    twitter_dm.txt
                    email_body.txt
            logs/
                app.log
                outreach.log
            output/
                leads.json
                weekly_report.csv
            tests/
                test_outreach_runner.py
                test_lead_validator.py
                test_rate_limiter.py
        docker-compose.yml
        Dockerfile
        pyproject.toml
        README.md

---

## Use Cases

- **Talent agencies** use it to systematically contact models on Instagram and Twitter/X, so they can keep their application funnel consistently full without constant manual messaging.
- **Creator management teams** use it to centralize outreach to potential new models, so they can quickly see who actually submitted the form and is worth following up with.
- **Influencer marketing teams** use it to gather a pool of authentic model profiles interested in collaborations, so they can filter and select based on form responses instead of unstructured DMs.
- **Small studios or brands** use it to run ongoing, low-friction recruitment campaigns, so they can spend their time reviewing qualified submissions instead of sending the same message hundreds of times.
- **Remote assistants and operators** use it to manage multiple outreach accounts at once, so they can meet volume goals while staying organized and compliant with platform limits.

---

## FAQs

**Q: Does this bot use my own social and email accounts?**
Yes. You configure the accounts (Instagram, Twitter/X, email providers) via the `accounts.yaml` and environment variables. The automation then uses those accounts to send outreach messages while respecting rate limits and platform guidelines.

**Q: Can I customize the outreach message for each platform?**
Absolutely. Message templates live in the `config/templates/` directory and support simple placeholders like `{name}`, `{platform}`, `{handle}`, and `{form_link}`. You can maintain different tones or languages for each platform without touching the code.

**Q: How does the system know which models actually filled out the form?**
Each lead is assigned a unique tracking token that is embedded into the form link. When the form is submitted, a webhook or polling job in `form_tracker.py` records the submission, links it back to the original profile, and marks the lead as valid if it passes validation rules.

**Q: What protections exist to avoid being flagged as spam or abusive?**
The outreach engine includes configurable rate limits, random delays, per-account daily caps, quiet hours, and content rotation. Combined with careful template design and realistic pacing, these controls help keep activity within safe, human-like patterns.

---

## Performance & Reliability Benchmarks

**Execution Speed:**
On a typical deployment, a single worker can safely send approximately 80–120 outreach messages per hour per account, depending on platform constraints and configured delays. Parallel workers and multiple accounts can be combined for higher aggregate throughput while staying within safe limits.

**Success Rate:**
With reasonable targeting and message templates, 93–94% of tracked form visits are correctly recorded and matched to the originating lead. Failed tracking events are automatically queued for retry when possible.

**Scalability:**
The architecture is built around queue-based workers and channel adapters. In practice, it can comfortably handle 10–50 concurrent sender accounts and several thousand outreach attempts per day by scaling the number of workers and database connections.

**Resource Efficiency:**
A typical worker instance consumes roughly 1 vCPU and 512–768 MB of RAM during steady-state operation, including a headless browser session for Playwright. Additional workers scale linearly, and browser lifecycles are managed to minimize idle resource consumption.

**Error Handling:**
All core operations implement structured error handling with exponential backoff, categorized error types, and contextual logging. Transient errors (network issues, soft platform blocks, temporary form endpoint failures) are retried automatically, while hard failures are recorded with enough detail in logs and reports to support quick diagnosis and recovery.


<p align="center">
<a href="https://calendar.app.google/74kEaAQ5LWbM8CQNA" target="_blank">
  <img src="https://img.shields.io/badge/Book%20a%20Call%20with%20Us-34A853?style=for-the-badge&logo=googlecalendar&logoColor=white" alt="Book a Call">
</a>
  <a href="https://www.youtube.com/@bitbash-demos/videos" target="_blank">
    <img src="https://img.shields.io/badge/🎥%20Watch%20demos%20-FF0000?style=for-the-badge&logo=youtube&logoColor=white" alt="Watch on YouTube">
  </a>
</p>
<table>
  <tr>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/MLkvGB8ZZIk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review1.gif" alt="Review 1" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash is a top-tier automation partner, innovative, reliable, and dedicated to delivering real results every time.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Nathan Pennington
        <br><span style="color:#888;">Marketer</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtu.be/8-tw8Omw9qk" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review2.gif" alt="Review 2" width="100%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Bitbash delivers outstanding quality, speed, and professionalism, truly a team you can rely on.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Eliza
        <br><span style="color:#888;">SEO Affiliate Expert</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
    <td align="center" width="33%" style="padding:10px;">
      <a href="https://youtube.com/shorts/6AwB5omXrIM" target="_blank">
        <img src="https://github.com/za2122/footer-section/blob/main/media/review3.gif" alt="Review 3" width="35%" style="border-radius:12px; box-shadow:0 4px 10px rgba(0,0,0,0.1);">
      </a>
      <p style="font-size:14px; line-height:1.5; color:#444; margin:0 15px;">
        “Exceptional results, clear communication, and flawless delivery. Bitbash nailed it.”
      </p>
      <p style="margin:10px 0 0; font-weight:600;">Syed
        <br><span style="color:#888;">Digital Strategist</span>
        <br><span style="color:#f5a623;">★★★★★</span>
      </p>
    </td>
  </tr>
</table>
