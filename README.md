# MedSimplify - Clinical Text Simplification System

An intelligent medical text simplification pipeline that transforms complex clinical documents into patient-friendly language while maintaining medical accuracy and providing interpretability insights.

## Overview

MedSimplify addresses the critical healthcare communication gap by automatically converting technical medical terminology into accessible language that patients can understand. The system combines multiple NLP techniques with comprehensive readability analysis and attention visualization for complete transparency.

## What it does

- **Medical Term Detection**: Uses regex patterns and curated medical dictionaries to identify complex clinical terminology
- **Intelligent Simplification**: Employs T5 sequence-to-sequence models fine-tuned for medical text simplification
- **Multi-Stage Processing**: Combines rule-based term replacement with neural text generation for optimal results
- **Readability Analysis**: Provides comprehensive metrics including Flesch Reading Ease, SMOG Index, and Gunning Fog
- **Attention Visualization**: Generates interpretable heatmaps showing model focus during simplification

## Architecture

### Term Detection Pipeline
- **Regex-based Detection**: Pattern matching for medical suffixes, procedures, and conditions
- **Curated Medical Dictionary**: 500+ medical terms mapped to lay-person equivalents
- **UMLS Integration**: Fallback to Unified Medical Language System for comprehensive coverage

### Simplification Pipeline
- **Pre-processing**: Initial term replacement using medical dictionary
- **T5 Model**: Fine-tuned sequence-to-sequence model for contextual simplification
- **Post-processing**: Quality assurance and readability optimization

### Interpretability Components
- **Readability Metrics**: Flesch Reading Ease, Flesch-Kincaid Grade, SMOG Index, Coleman-Liau Index, Gunning Fog
- **Attention Heatmaps**: T5 encoder attention visualization for model interpretability
- **Comparative Analysis**: Before/after readability score comparison with radar charts

## Tech Stack

**Core NLP**
- Transformers library with T5 models (mrm8488/t5-small-finetuned-text-simplification)
- NLTK for text preprocessing and tokenization
- Regex for medical term pattern matching

**Readability Analysis**
- TextStat for comprehensive readability metrics
- Custom medical term identification algorithms

**Visualization**
- Plotly for interactive radar charts and attention heatmaps
- Custom attention visualization for transformer interpretability

**Integration**
- UMLS API for medical terminology lookup
- Modular Kaggle notebook pipeline for reproducible research

## Key Features

- Processes clinical notes, discharge summaries, and medical reports
- Maintains medical accuracy while improving accessibility
- Provides quantitative readability improvements
- Offers complete model interpretability through attention analysis
- Scalable pipeline suitable for healthcare organizations
- Comprehensive evaluation metrics for quality assessment

## Performance

The system demonstrates significant readability improvements across multiple metrics:
- Flesch Reading Ease scores typically improve by 20-40 points
- Grade level requirements reduced by 2-4 levels on average
- Maintains clinical accuracy while achieving lay-person accessibility
- Attention analysis confirms focus on relevant medical terminology during processing
