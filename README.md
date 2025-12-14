# Listening to Recovery  
**Where Tone Meets Transformation**

## Project Overview
**Listening to Recovery** is a data-driven analytics project that transforms unstructured addiction recovery narratives into structured, actionable insights. By analyzing real recovery stories, this project uncovers recurring emotional, behavioral, and experiential patterns across the addiction–recovery journey.

The goal is to reduce isolation, set realistic recovery expectations, and support more informed decision-making for individuals, families, and healthcare providers.

---

## Problem Statement
Addiction recovery journeys are deeply personal, non-linear, and poorly captured by traditional data sources. Current challenges include:
- Scattered and unstructured recovery information  
- Limited accessibility to lived experiences  
- Lack of data-driven understanding of recovery stages and setbacks  

Individuals in recovery often ask:
- *What will my recovery journey realistically look like?*  
- *When do setbacks typically occur?*  
- *What strategies have worked for others?*  

This project addresses these gaps by converting human stories into structured analytical insights.

---

## Data Source
- **51 addiction recovery narratives**
- Scraped transcript data from *Texas Picture Documentaries* (YouTube)
- Narratives span the full recovery lifecycle, from first use to long-term maintenance

---

## Methodology

### 1. Journey Stage Identification
We identified **9 distinct recovery stages**:
1. Background  
2. First Use  
3. Escalation  
4. Rock Bottom  
5. Turning Point  
6. Treatment  
7. Early Recovery  
8. Relapse  
9. Maintenance  

- Stage detection performed using **GPT-4o-mini**
- Results validated through direct quote alignment
- Enables mapping of each individual’s full recovery journey

---

### 2. Sentiment Analysis (and Its Limitations)
- Initial sentiment analysis performed using **DistilBERT**
- Findings revealed sentiment alone is misleading:
  - Optimism can appear early, even during crisis
  - Critical moments may sound emotionally calm
- Conclusion: **Sentiment ≠ Recovery Progress**

This led to the development of a more robust severity-based framework.

---

### 3. Event-Driven Severity Scoring
To overcome sentiment limitations, we designed a **rule-based severity metric**:

**Severity Score =**  
`(Weighted Clinical Events × Frequency Multiplier) + Diversity Bonus`

Key elements:
- Events weighted by clinical severity
- Repeated trauma increases severity
- Multiple crisis types compound impact (mental health, legal, housing)

This approach avoids LLM “ceiling effects” and better distinguishes moderate vs. extreme recovery crises.

---

## Key Insights

### Turning Points
- **70%** of individuals cite **self-realization** as their primary turning point
- Family pressure triggers recovery in only **6%**
- Internal motivation outpaces external pressure by **12×**

**Implication:** Recovery interventions should prioritize self-awareness over coercion.

---

### Rock Bottom Patterns
- Mental health crises present in **92%** of journeys
- Family relationship breakdown in **86%**
- Physical health consequences ranked lowest as root causes

**Implication:** Addiction is primarily a mental health condition, not a physical one.

---

### Entry into Addiction
- **47%** began with self-medication, not recreation
- **39%** driven by boredom and lack of purpose
- Medical prescriptions triggered < **5%** of cases in this sample

**Implication:** Prevention must address emotional coping and purpose, not only substance access.

---

## Recovery Pathways
Despite personal differences, recovery patterns repeat:

- **Turning Point:** Self-realization > external intervention  
- **Treatment:** Structured inpatient care + peer support most effective  
- **Maintenance:** Community engagement and ongoing meetings sustain recovery  

A Sankey-based pathway analysis highlights the most frequent and successful recovery routes.

---

## Tools & Technologies
- **Python** (data processing, analysis)
- **GPT-4o-mini** (journey stage classification)
- **DistilBERT** (sentiment analysis)
- Rule-based analytics for severity scoring
- Data visualization for pattern discovery

---

## Future Scope & Improvements
- Expand dataset diversity (multilingual & cross-cultural narratives)
- Introduce temporal models (LSTM / Transformers) to predict relapse likelihood
- Integrate speech & tone analysis from audio data
- Build clinician-facing interactive dashboards
- Develop real-time relapse risk detection systems

---

## Team
- Abhiroop K  
- Alina H  
- Keerti R  
- Manoranjith A  
- Rohan D  
- Simoni D  

---

## Disclaimer
This project is for **academic and analytical purposes only**.  
It is **not** intended to replace professional medical or psychological care.

---

## Acknowledgements
- Texas Picture Documentaries (YouTube)
- Individuals who shared their recovery stories

---

*Listening to Recovery demonstrates how human narratives, when analyzed responsibly, can inform empathy-driven and data-backed recovery insights.*
