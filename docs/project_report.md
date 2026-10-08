# LEADWISE — Project Report

## 1. Executive Summary
LEADWISE is a Streamlit-based sales lead-scoring decision-support application. It prioritizes prospects using deterministic scoring across firmographic fit, engagement, buying intent, and recency, then classifies them as Hot, Warm, or Cold. An optional Gemini layer explains structured results without changing the deterministic ranking.

## 2. Professor Use Case
Use Case #7 — Sales lead-scoring assistant (App): lead data upload/entry, scoring against firmographic + engagement signals, Hot/Warm/Cold tiering, and CRM-style export.

## 3. Business Problem
Sales teams often have more leads than they can contact with equal intensity. LEADWISE helps sales users prioritize limited attention using transparent, repeatable scoring.

## 4. Target Users
Primary end users: SDRs, account executives, sales managers and revenue-operations teams. A potential paying customer is a B2B company using a CRM or sales platform.

## 5. Methodology
The score combines four components: Firmographic Fit (30%), Engagement (30%), Intent (25%), and Recency (15%). Component scores are normalized to a 0–100 range and combined into an Overall Lead Score. Tiers are Hot (80+), Warm (60–79.99), and Cold (<60).

## 6. AI Design
Gemini is used only as an explanatory assistant. The system prompt prohibits invented lead facts, score overrides, certainty about conversion, and autonomous outreach decisions. If the API is unavailable, the deterministic analytics remain available.

## 7. Application Modules
Home, Executive Dashboard, Lead Ranking, Lead Analysis, Lead Profile, Prioritization Simulator, What-If Analysis, AI Sales Assistant, Data Validation and CRM-style Export.

## 8. Validation
The validation layer checks required columns, missing values, duplicate IDs, non-negative numeric fields, binary decision-maker flags, and controlled categorical values. A deliberately invalid dataset demonstrates the checks.

## 9. Scenario Analysis
Users can test Balanced, Engagement First, Intent First and Fresh Activity strategies. A What-If interface allows users to adjust the four scoring weights; weights are normalized automatically.

## 10. Testing
The project includes 10-lead demonstration data, a 250-lead scalability dataset, and an invalid test dataset. Core score calculation, ranking, tiering, scenario analysis and validation are designed to be deterministic and reproducible.

## 11. Responsible AI
The application is decision support, not autonomous sales automation. Human users remain accountable for outreach decisions. Synthetic data is used for demonstration. External AI use should be disclosed when real lead data is connected.

## 12. RAG vs Fine-Tuning
The prototype does not require RAG or fine-tuning because its main task is structured analytics. RAG could be added later for product documentation, account plans, sales playbooks and CRM notes. Fine-tuning could be considered for organization-specific language or workflows after collecting validated examples.

## 13. SWOT
Strengths: transparent scoring, scenario analysis, explainability, export.
Weaknesses: synthetic demo data, scoring quality depends on input quality, external AI dependency for explanations.
Opportunities: CRM integration, real-time intent signals, multilingual support, account intelligence.
Threats: established CRM vendors, API price/model changes, privacy regulation, poor-quality lead data.

## 14. Competitors
Real-world competitors include Salesforce Sales Cloud and HubSpot. LEADWISE differs as a focused academic prototype centered on transparent multi-criteria lead prioritization, scenario analysis and an optional explanation layer.

## 15. Critical Thinking
The app should not be trusted to guarantee conversion, automatically contact prospects, or infer sensitive personal characteristics. A high score is prioritization evidence, not a probability guarantee.

## 16. Limitations
The current demonstration uses synthetic data; no CRM is connected; Gemini availability depends on external API access; scoring weights are configurable assumptions rather than statistically trained conversion probabilities.

## 17. Future Roadmap
CRM integration, validated historical conversion data, calibration against actual outcomes, RAG over sales playbooks, account-level intelligence, real-time intent feeds, role-based access, audit trails and enterprise deployment.

## 18. Conclusion
LEADWISE demonstrates how deterministic analytics and generative AI can be combined without surrendering decision control to an LLM. The result is a transparent, scenario-aware sales prioritization workflow suitable for a prototype and extensible toward enterprise sales operations.
