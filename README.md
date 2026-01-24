# Human-Centered Auditing of LLMs for Local Government Reporting

This repository contains the data and implementation for a human-centered evaluation and auditing framework designed to assess the capability of Large Language Models (LLMs) in automating local journalism tasks. Specifically, we investigate the model's ability to identify newsworthy topics from municipal proceedings and generate professional-grade headlines.

## Project Overview
Traditional local journalism is facing a resource crisis. This project evaluates whether LLMs can augment newsrooms by:
1.  **Extracting** salient information from city council agendas and meeting transcripts.
2.  **Generating** news headlines that meet professional journalistic standards.
3.  **Prioritizing** topics based on local impact and newsworthiness.

Our pipeline includes a comparative study where LLM outputs are audited against professional standards via crowd-sourced human evaluation.

---

## Directory Structure

```text
.
├── ___input/                   # Primary raw data sources
│   ├── agenda_url/             # Source URLs for city council agendas
│   ├── audio/                  # Meeting recordings (.wav) for transcription
│   └── evaluations/            # Raw human evaluation responses from Prolific
│
├── __src/                      # Modular Research Pipeline (Jupyter Notebooks)
│   ├── mod1_agenda_proc/       # Scraping and cleaning of PDF/text agendas
│   ├── mod2_trans_proc/        # Speech-to-text and segmenting meeting audio
│   ├── mod3_llm_gen/           # Prompt engineering for headline generation
│   ├── mod4_ranking/           # Processing model and human ranking data
│   └── mod5_llm_auditing/      # Statistical analysis and metric calculation
│
├── _interim/                   # Processed data at each pipeline stage
│   └── ...                     # (See notebooks for specific step outputs)
│
└── results/                    # Final artifacts for the paper
    ├── average_rank.pdf        # Plot of average true rank of LLM and expert selected topics
    ├── headline_rank_diff.pdf  # Plot of average rank difference between LLM-generated and expert-written headlines for the same topic
    └── recall_rate.pdf         # Plot of top-3/5 topic recall rate from LLM and expert selected topics
```

