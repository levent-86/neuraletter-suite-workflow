# NeuraLetter Suite: Workflow - Automate Hyper-Personalized B2B Outreach from CSV using AI

This workflow is the engine of the [NeuraLetter Suite: Scrap](https://chromewebstore.google.com/detail/neuraletter-suite-scrap/njdhnogadpoafagjibjcopbngknjiikl?authuser=0&hl=tr). It automates high-quality B2B cold outreach by using AI to write hyper-personalized emails based on your leads' company data.

Unlike standard bots, this workflow utilizes a **Fisher-Yates inspired randomization algorithm** to mimic human behavior, keeping your sending reputation safe and your emails out of the spam folder.

### Who is it for
- **Solopreneurs & Bootstrappers:** Founders looking to acquire their first B2B customers without burning cash on ads.
- **Freelancers & Agencies:** Professionals who need a "set-and-forget" automated sales rep running in the background to fill their pipeline.
- **Growth Engineers:** Technical marketers who value stealthy, algorithm-backed automation over expensive, rigid SaaS tools.
- **Cost-Conscious Founders:** Businesses wanting to replace expensive monthly subscriptions (like Apollo or Instantly) with a powerful self-hosted system.

### Good to know
- **Self-Hosted Requirement:** Due to its reliance on local file system operations (CSV read/write) this workflow can work on self-hosted only.
- **Beginner Friendly:** Every single node in this workflow contains detailed **Sticky Notes (Steps #1 - #10)**. You don't need to be an expert; just follow the notes inside the editor!
- **Safe Volume:** Designed to send approx. 375 - 750 emails per month approximately with a single email account, staying well within safe limits.
- **Cost Efficient & Flexible:** Uses flexible access to various LLMs and your preferred **SMTP/Email Service** for sending.

### Key Features at a Glance
- **🎣 Advanced Bot Evasion:** Utilizes a custom, Fisher-Yates inspired scheduling algorithm to create unpredictable delays, masking robotic sending patterns from sophisticated spam filters.
- **🧠 LLM Agnostic Personalization:** Allowing seamless switching between top models (like Gemini, Claude, or GPT) for hyper-personalized content and subject line generation.
- **🛡️ Duplicate Sending Prevention:** Reads and updates a mandatory `is_sent` column in your CSV, ensuring no lead receives the same email twice.
- **🌐 Multilingual Outreach:** Automatically detects the target company's language from the `About` text and generates the entire subject line in that specific language.
- **✨ Guided Setup:** Extensively documented with **Sticky Notes (Steps #1 - #10)** inside the workflow, making advanced configuration comfortable for all users.

### How it works
1. **Smart Scheduling:** The workflow wakes up at set intervals. It uses a custom **Fisher-Yates inspired algorithm** to generate an unpredictable, human-like delay (e.g., waiting 13 mins one time, 48 mins the next) to evade bot detection.
2. **Data Processing:** It reads your local CSV file (compatible with [NeuraLetter Suite: Scrap](https://chromewebstore.google.com/detail/neuraletter-suite-scrap/njdhnogadpoafagjibjcopbngknjiikl?authuser=0&hl=tr) extension), filters out leads that have already been contacted (`is_sent=FALSE`), and picks one target.
3. **AI Personalization:**
    - **Node 1 (Content):** AI analyzes the prospect's "About" section and writes a bespoke email explaining how *your* product solves *their* specific problems.
    - **Node 2 (Context):** AI detects the prospect's language (e.g., English, German, Spanish) and generates a high-conversion Subject Line in that language.
4. **Execution:** The personalized email is sent (with optional attachments), and the lead is marked as `TRUE` in your CSV file to prevent duplicate sending.

### How to use
1. **Prepare Data:** You need a CSV file with headers: `Company Name`, `Email`, `About`, and `is_sent`. (You can easily generate this using the [NeuraLetter Suite: Scrap](https://chromewebstore.google.com/detail/neuraletter-suite-scrap/njdhnogadpoafagjibjcopbngknjiikl?authuser=0&hl=tr) Chrome extension).
2. **Setup:** Double-click the nodes to add your AI API Key and Email credentials.
3. **Customize:** Follow the **Sticky Notes** on the AI nodes to insert your own Product Name and Value Proposition into the prompts.
4. **Run:** Activate the workflow and let it run in the background!

### Requirements
- **n8n** (Self-hosted)
- **AI API Key**
- **Email Account** (with SMTP service)
- A local **CSV file** with lead data

### Customising this workflow
- **Multi-lingual:** The workflow is already set up to detect languages. You can tweak the "AI for Language Decision" node to support specific dialects or regions.
- **Attachments:** Use the optional "Get E-mail Attachment" node to send dynamic PDF catalogs.

Questions? Visit [NeuraLetter.com](https://neuraletter.com) website, or reach out via forum: [Node](https://community.n8n.io/u/node/summary)

---
### DISCLAIMER / LIABILITY WAIVER
This automation workflow is provided **free of charge and "as-is"**.
The User accepts **sole responsibility** for any and all risks and consequences, including but not limited to material and immaterial damages, loss, suspension of email accounts (banning), or reputational harm, that may arise **before, during, or after the use** of this workflow. The party providing the workflow (the developer) holds no liability whatsoever.
