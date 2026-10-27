# MediConnect — AI-Powered Healthcare Platform

> An AI-powered Doctor Finder + Symptom Checker built entirely using Claude AI.  
> Built as a job assessment project for **AI Growth & Automation Associate** position at gokulinfocare.com

---

## 🌐 Live Demo
[View on Claude Artifacts](https://claude.ai/artifact/8GMi8NG1DAxscd6Mj1gpG7)

---

## 🚀 Features

### 1. AI Symptom Checker
- Select from 25 common symptoms
- Rule-based AI engine cross-references symptom combinations
- Returns: likely conditions with probability scores, urgency level, specialist recommendation, self-care tips
- Covers 8 medical categories: Cardiology, Neurology, Respiratory, Dermatology, Orthopaedic, Gastro, Psychiatry, ENT

### 2. Doctor Finder
- 12 verified doctors across 9 specialties
- Filter by specialty, search by name/keyword, filter by availability
- Doctor cards: rating, experience, consultation fee, location, tags

### 3. Appointment Booking
- Click any doctor → booking modal opens
- Select a time slot → confirm → toast notification

### 4. Professional UI
- Dark mode toggle (persisted in localStorage)
- Fully responsive (mobile + desktop)
- Smooth animations and transitions
- Single-page app with hash-based routing

---

## 🤖 How AI is Used

### Claude AI as the Core Tool
The **entire project** was built using Claude AI (claude.ai):
- UI/UX design decisions
- All HTML, CSS, JavaScript code
- The symptom analysis logic
- Doctor database content
- Iterative debugging and fixes

### The Symptom Checker AI Engine
The AI decision-making works as a **rule-based inference engine**:

```
User selects symptoms
        ↓
AI_RULES array is evaluated (8 medical rules)
        ↓
Each rule has a match() function that checks symptom combinations
        ↓
First matching rule fires → returns:
  - 3 possible conditions with probability %
  - Urgency level (high / medium / low)
  - Recommended specialist
  - Self-care tips
        ↓
If no rule matches → DEFAULT_RULE fires (General Physician)
```

**Example:** User selects "Chest Pain" + "Heart Palpitations"
→ Rule match: cardiac symptoms detected
→ AI returns: Cardiac Arrhythmia (72%), Angina (58%), Anxiety-Induced (45%)
→ Urgency: 🚨 HIGH — "Seek immediate medical attention"
→ Specialist: Cardiologist
→ Find Specialist button → filters doctors to Cardiologists

This is the same logic used in real triage systems — mapping symptom clusters to likely diagnoses.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure |
| CSS3 | Styling, animations, dark mode |
| Vanilla JavaScript | All interactivity and AI logic |
| Google Fonts (Sora + Inter) | Typography |
| Claude AI | Entire build — design, code, logic, content |
| Rule-based AI Engine | Symptom → diagnosis inference |
| No backend / No API key | All logic runs client-side in the browser |

---

## 📁 Project Structure

```
mediconnect/
│
├── index.html          # Complete single-file app (HTML + CSS + JS)
└── README.md           # This file
```

Single-file architecture — no dependencies to install, no build step needed.

---

## ▶️ How to Run Locally

1. Download/clone this repository
2. Open `index.html` in any modern browser
3. That's it — no server, no npm install needed

---

## 🧠 AI Decision Flow (for video demo)

Walk through this during your demo:

1. Go to **Symptom Checker**
2. Select: `Chest Pain` + `Heart Palpitations`  
   → AI detects cardiac pattern → outputs HIGH urgency + Cardiologist
3. Select: `Cough` + `Fever` + `Fatigue`  
   → AI detects respiratory pattern → outputs LOW urgency + General Physician
4. Select: `Anxiety` + `Insomnia`  
   → AI detects mental health pattern → outputs MEDIUM urgency + Psychiatrist
5. Click **Find Specialist** → auto-filtered doctor list
6. Click a doctor → booking modal → select slot → confirm → toast

---

## 📋 Prompt Engineering (Summary)

This project was built through iterative prompt engineering with Claude AI:

1. **Initial prompt:** "Build an AI-powered healthcare website with Doctor Finder and Symptom Checker"
2. **Design prompt:** "Use a professional medical UI with blue accent, Sora + Inter fonts, dark mode support"
3. **AI logic prompt:** "Build a rule-based symptom checker that maps symptom combinations to conditions with probability scores and specialist recommendations"
4. **Data prompt:** "Create 12 realistic Indian doctors across 9 specialties with ratings, fees, locations"
5. **Bug fix prompts:** Navigation hash routing conflicts, `onclick` return values
6. **Refinement:** Iterative fixes for mobile responsiveness, modal behavior, toast animations

Full prompt documentation available separately.

---

## ⚠️ Disclaimer

This is a prototype built for assessment purposes. It is not a substitute for professional medical advice. Always consult a qualified healthcare professional for diagnosis and treatment.

---

**Built with Claude AI · Submitted to gokulinfocare.com**
