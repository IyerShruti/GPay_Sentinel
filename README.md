# GPay Sentinel 🛡️

Detecting the Unseeable: Real-Time Behavioral Security for Coached Scams

GPay Sentinel is an intelligent security intelligence layer designed to protect users from "coached scams." Unlike traditional security that monitors what is being sent, Sentinel monitors how it is being sent. By analyzing behavioral biometrics—specifically transaction velocity and hesitation—Sentinel provides a "Guardian Angel" for the GPay ecosystem.

## Inspiration

While our technical security (encryption, 2FA) is stronger than ever, the human element remains vulnerable. Scammers now use "coaching" tactics—staying on a call with a victim to guide them through a fraudulent transaction. As a recent Master’s graduate (May 2025), I wanted to build a system that identifies the psychological pressure and hesitation inherent in these scams before the money ever leaves the account.

## What it does

GPay Sentinel functions as a high-fidelity "body language reader" for digital payments:

Behavioral Monitoring: It tracks the "rhythm" of a user's transaction flow.

The 1.5x Hesitation Rule: If a user’s interaction speed becomes 1.5x slower than their personal historical baseline, a "Hesitation Spike" is triggered.

AI Voice Briefing: The system sends raw behavioral data to Gemini 3 Flash, which generates a real-time audio briefing for security operators, explaining the likely nature of the scam.

Resilient Defense: If cloud connectivity is lost, the system switches to a local Edge Logic layer to maintain protection.

## How I built it

The project is built as a hybrid intelligence system:

The Brain: An ensemble of XGBoost for fast local pattern recognition and Gemini 3 Flash for deep contextual reasoning.

The Logic: Built using Python (Scikit:learn) and Jupyter Notebooks for data analysis.

The Operator Interface: A React:based dashboard featuring the Web Speech API for hands:free AI briefings.

## Challenges I ran into

Overfitting: My initial machine learning models achieved near:perfect accuracy on training data but struggled with real:world "noise" and generalization. I solved this by pivoting to a Hybrid Heuristic:AI approach, using a robust 1.5x threshold combined with Gemini's reasoning.

API Quota Limits: Reaching the Gemini "Free Tier" limit during the final hours of testing was a critical hurdle. This led to the creation of the "Edge Mode" Fallback, which ensures the 1.5x Hesitation Rule works locally even without an API connection.

## Accomplishments that I'm proud of

Successfully translating a psychological concept (hesitation) into a quantifiable security metric.

Developing a "High Availability" AI architecture that turns a technical failure (API throttling) into a reliability feature.

Creating a tool that protects the person, not just the account.

## What we learned

I learned that production:grade AI requires more than just a smart model; it requires resilience. Handling overfitting taught me that "simpler is often better" for core logic, while Gemini taught me that Generative AI is the perfect tool for bridging the gap between raw data and human decision:making.

## What's next for GPay Sentinel

Multimodal Biometrics: Integrating touch:pressure and gyroscope data to detect "stress tremors."

Guardian Angel Mode: A proactive UI intervention that asks the user, "Are you being coached on a call?" based on real:time detection.

Network Intelligence: Incorporating SIM:swap detection and VoIP metadata to increase the confidence of scam alerts.

## Built With

React.js, Node.js, Gemini 3 Flash API, XGBoost, Python (Scikit:learn), Web Speech API, Tailwind CSS, Google AI Studio, and a custom Local Edge Logic engine.

## Getting Started

Clone the repo.

Add your API Key: Create a .env file in the root directory and add GEMINI_API_KEY=your_key_here.

Run the Notebook: Open GPay_Sentinel_Analysis.ipynb to see the logic behind the 1.5x Hesitation Rule.

View the Documentation: See Technical_Briefing.pdf for a deep dive into the architecture.
