# 🌐 Bhasha-Arogya: Cross-Language Health Bridge  

*Breaking healthcare language barriers, one symptom at a time.*  

![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)  
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)  
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white)  

Breaking healthcare language barriers, one symptom at a time.






🩺 Why This Matters

Language divides often cost lives. A villager in rural Bengal describing “আমার বুক ধড়ফড় করছে” may not be fully understood by an English-speaking doctor.

Bhasha-Arogya bridges this gap. It’s an AI-driven health assistant that:

Transforms colloquial Bengali symptom descriptions into structured, doctor-friendly data

Highlights critical red flags automatically

Offers safe, general OTC guidance with disclaimers

Translates doctor’s instructions back into simple Bengali

⚠️ Important Note: This is a prototype intended for research & demonstration. It is not a certified medical product and must not replace professional diagnosis or treatment.

✨ Core Features
Feature	What it Does	Why it Matters
🧠 Symptom Understanding	Extracts symptom, severity, duration, red flags from Bengali free text	Turns messy patient input into structured medical data
🚨 Red Flag Alerts	Detects urgent signals like severe dehydration or chest pain	Helps clinicians prioritize emergency cases
💊 AI OTC Suggestions	GPT-based, non-prescriptive general advice for minor issues	Provides patients with safe, educational next steps
🔄 Doctor ↔ Patient Translation	Converts medical English advice into simple Bengali	Builds trust and health literacy
🛠️ Tech Stack

Backend: Python + FastAPI (async-ready APIs)

Frontend: React + TypeScript

AI/NLP: OpenAI GPT API + Bengali regex/lexicon parsers

Auth (Optional): JWT / OAuth2

⚡ Getting Started
Prerequisites

Python 3.9+

Node.js & npm

OpenAI API Key

1. Clone the Repo
git clone https://github.com/<your-username>/cross-language-healthbot.git
cd cross-language-healthbot

2. Backend Setup
cd backend
pip install -r requirements.txt

# Set your OpenAI Key
# macOS/Linux
export OPENAI_API_KEY="your_key_here"
# Windows
setx OPENAI_API_KEY "your_key_here"

# Run FastAPI
uvicorn app.main:app --reload --port 8000


API Docs → http://localhost:8000/docs

3. Frontend Setup
cd ../frontend
npm install
npm start


App UI → http://localhost:3000

👩‍⚕️ End-to-End User Journey

Patient describes symptoms in Bengali:
"আমার পেটে খুব ব্যথা, বমি হচ্ছে, জ্বর গতকাল থেকে।"

Backend parses & structures data:

{
  "symptoms": ["abdominal pain", "vomiting", "fever"],
  "severity": "severe",
  "duration": "1 day",
  "red_flags": []
}


AI Suggestion: Rest, hydration, OTC paracetamol (with disclaimers).

Doctor enters English advice → system translates to Bengali for patient clarity.

🔌 Example API

Endpoint: POST /api/parse-symptoms

Request:

{
  "text": "মাথা ব্যাথা এবং সারা শরীরে জ্বর আছে।"
}


Response:

{
  "structured_data": {
    "symptoms": ["headache", "fever"],
    "severity": "mild",
    "duration": "unknown",
    "red_flags": []
  },
  "ai_advice": "For headache and fever, rest and hydration are recommended. Paracetamol may help. See a doctor if symptoms worsen.",
  "translated_advice": "মাথাব্যথা এবং জ্বরের জন্য বিশ্রাম এবং জলখাবার সুপারিশ করা হয়। প্যারাসিটামল সাহায্য করতে পারে। উপসর্গ খারাপ হলে ডাক্তার দেখান।"
}

📂 Project Layout
cross-language-healthbot/
├── backend/
│   ├── app/
│   │   ├── main.py          # FastAPI entrypoint
│   │   ├── models.py        # Data models
│   │   ├── nlpparser.py     # Bengali NLP parsing
│   │   └── ai_helper.py     # GPT integration
│   ├── requirements.txt
│   └── README.md
└── frontend/
    ├── src/
    │   ├── components/      
    │   └── App.tsx
    ├── package.json
    └── README.md

🤝 Contributing

Want to help break healthcare language barriers? Contributions welcome!

Fork the repo

Create a branch: git checkout -b feature/MyFeature

Commit: git commit -m 'Add my feature'

Push: git push origin feature/MyFeature

Open a PR

📜 License

This project is licensed under the MIT License. See the LICENSE file.

👨‍💻 Authors

Baishakhi Sing
Email:baishakhi.sing154@gmail.com
Srizoni Maity
Email:im.srizoni@gmail.com


