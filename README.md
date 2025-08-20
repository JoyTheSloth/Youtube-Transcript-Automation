# YouTube Transcript Automation

Automate the process of fetching, cleaning, and storing YouTube video transcripts into Google Sheets using **n8n** + **LLMs**.

## 📌 Features

* 🔄 Automatically triggers on schedule.
* 📥 Fetches video links from Google Sheets.
* 📝 Extracts & cleans YouTube video transcripts.
* 🤖 Uses AI (Google Gemini / LLM) to summarize or optimize transcripts.
* ✨ Cleans and reformats AI outputs (removes `\n`, `**`, etc.).
* 📊 Updates processed titles and transcripts back into Google Sheets.

## ⚙️ Workflow Overview

1. **Schedule Trigger** – starts the automation.
2. **Get Rows (Google Sheets)** – fetches video links.
3. **Loop Over Items** – processes each link.
4. **Extract Link** – parse and clean YouTube video ID.
5. **Get Transcripts** – fetch raw transcripts from YouTube.
6. **Extract & Combine Transcripts** – merge into full text.
7. **Basic LLM Chain (Gemini / OpenAI)** – process transcripts (summarization, title generation, etc.).
8. **Code Node** – clean and format AI-generated text.
9. **Manage Output** – structure results.
10. **Update Row in Sheet** – write back clean titles & transcripts.

## 🛠️ Tech Stack

* [n8n](https://n8n.io) – Workflow automation.
* Google Sheets API – Store input links & outputs.
* YouTube Transcript API – Extract raw captions.
* Google Gemini (or OpenAI) – AI processing & summarization.
* JavaScript (Code Nodes) – cleaning & formatting.



## 📸 Screenshots

<img width="1514" height="319" alt="image" src="https://github.com/user-attachments/assets/0c688d10-65d2-45e1-8241-39c4de555291" />
<img width="1670" height="534" alt="image" src="https://github.com/user-attachments/assets/c6256c61-b0ad-4c97-bd45-8e57b3a8e47f" />
<img width="1666" height="641" alt="image" src="https://github.com/user-attachments/assets/6aa6ce74-e300-4b27-84c5-368f2e139578" />
<img width="1668" height="638" alt="image" src="https://github.com/user-attachments/assets/2dab921f-d821-4550-8798-94fda8b3a438" />
<img width="1478" height="500" alt="image" src="https://github.com/user-attachments/assets/af08a6ac-d0e1-448c-9a3f-7ae60bfb13aa" />

## 📌 Example Output

| Video Link                                     | Transcript (Summary)        | AI Titles                       |
| ---------------------------------------------- | --------------------------- | ------------------------------- |
| [https://youtu.be/xxxx](https://youtu.be/xxxx) | Short clean transcript here | 1. Title idea … 2. Title idea … |

## 🤝 Contributing

Pull requests are welcome! For major changes, please open an issue first to discuss what you’d like to change.



Would you like me to also **export your workflow JSON** into a `workflows/` folder template (so people can import it directly into n8n)?
