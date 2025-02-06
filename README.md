# Deciphering the Enigma: An Integrated Computational Pipeline for the Voynich Manuscript

This repository contains an integrated computational pipeline designed to tackle the enduring mystery of the Voynich Manuscript. The manuscript, a 240‑page codex of mysterious illustrations and undeciphered text, has long resisted conventional decipherment efforts. Our approach combines state‑of‑the‑art transformer models, evolutionary algorithms, network clustering, multimodal image‑text integration, and expert heuristic post‑processing to produce a unified candidate translation.

## Overview

Our pipeline is composed of the following main modules:
- **Data Acquisition and Pre‑Processing:**  
  High‑resolution multispectral scans from Yale’s Beinecke Rare Book & Manuscript Library are processed using deep learning‑based OCR (tailored to the Extensible Voynich Alphabet) to produce a complete transcription. The text is then segmented into thematic sections (botanical, astronomical, balneological, pharmaceutical, recipes) using a fine‑tuned ResNet‑50 model.

- **Transformer-Based AI Module:**  
  Synthetic parallel data is generated by “Voynich‑izing” sentences from a comparative corpus of medieval texts. Transformer models (GPT‑2 and T5) are fine‑tuned on this data using a curriculum learning strategy.

- **Evolutionary Algorithm Module:**  
  Candidate mappings of Voynich glyphs to Latin syllables are evolved using DEAP with a fitness function that combines frequency matching, syntactic coherence (via pretrained medieval Latin models), and expert heuristic feedback.

- **Network and Multimodal Integration Module:**  
  A full co‑occurrence network is constructed from the transcribed text, and clustering (via Louvain and spectral methods) identifies thematic communities. A CLIP‑like model is used to compute joint embeddings between text and images to ensure contextual alignment.

- **Expert Heuristic Post‑Processing:**  
  Rule‑based corrections are applied based on a database of medieval Latin grammar, common abbreviations, and scribal conventions. Automated expert scoring simulates human-in-the-loop feedback to guide further refinement.

- **External Validation:**  
  Statistical validation is performed by comparing candidate translations with an expanded corpus of verified medieval texts. Metrics such as conditional entropy, topic coherence, and Zipf’s law adherence are computed, and paleographic analysis confirms alignment with historical scribal patterns.

## Repository Structure

- `README.md`: This file.
- `main.py`: The main Python script for running the pipeline (see below).
- `Dockerfile`: Containerization file for reproducible deployment.
- `requirements.txt`: List of Python dependencies.
- `supplementary_documentation.txt`: Detailed technical documentation of methods and procedures.
- `validation_report.txt`: A simulated report of external validation metrics.

## Getting Started

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Oudemac/Voynich.git
   cd Voynich
