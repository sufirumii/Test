# Oncology Genomics Analyzer – Powered by google/gemma-3-27b-it

A single page web application that processes tumor genomic and clinical data using a multi-agent LLM pipeline. It parses key biomarkers, forecasts hypothetical trajectories, queries real-time recruiting clinical trials from ClinicalTrials.gov, and generates speculative summary vectors of possible therapy approaches — strictly for research and demonstration purposes.

Powered by google/gemma-3-27b-it:featherless-ai (Hugging Face inference)

## Features

- Clean glassmorphism interface with animated particle background
- Text input for genomic profile, cancer type, analysis depth, and prior treatments
- Real-time biomarker extraction (mutations, TMB, MSI, PD-L1, HRD, etc.)
- Projected biomarker trajectory visualization over 6–24 months
- Live recruiting trial matching via ClinicalTrials.gov API
- Ranked summary of hypothetical therapy vectors with confidence estimates, mechanisms, evidence, and risk notes
- Four interactive charts: mutation landscape, biomarker radar, trajectory forecast, benefit-risk scatter
- One-click PDF report export

## Important Disclaimer

This is a research prototype only — not a medical device, not for clinical use, and not intended to provide treatment recommendations.  
LLM outputs may contain inaccuracies or hallucinations.  
Trial matches are fetched live but must be independently verified.  
Always consult qualified medical professionals and tumor boards for real patient care.

## How to Run

1. Save the code as index.html  
2. Open the file in a modern browser (Chrome, Edge, or Firefox recommended)  
3. Paste genomic and clinical data into the main textarea  
4. Select cancer type and other options if desired  
5. Click ANALYZE & OPTIMIZE  

No server or installation required — everything runs client-side except the LLM inference and trial API calls.

## Sample Input
Cancer: Triple-negative breast cancer (TNBC), metastatic
Age: 44, Female
Genomics:

BRCA1 germline pathogenic variant (c.68_69delAG)
HRD score: 92 (high)
TMB: 28 mut/Mb (very high)
MSI: High (MSI-H)
PD-L1 CPS: 45
PIK3CA p.H1047R
MYC amplification

Prior therapy:

AC → T (neoadjuvant) → residual disease
Pembrolizumab + chemotherapy (first-line metastatic)
Sacituzumab govitecan → progression

Current: Liver and lung metastases, ECOG 1
text## Tech Stack

- HTML + CSS (glassmorphism design)  
- Vanilla JavaScript  
- Chart.js — visualizations  
- jsPDF — PDF export  
- Hugging Face Inference API — google/gemma-3-27b-it:featherless-ai  
- ClinicalTrials.gov API v2 — real-time trial data

## License

MIT License

Contributions, forks, and feedback are welcome.
