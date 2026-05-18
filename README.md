# Exploring OSHA Construction Accident Records with Multimodal AI Models

This project develops a multimodal AI framework for analyzing construction safety hazards using OSHA accident reports and construction site images. The framework combines text-based accident report analysis with image-based hazard detection to support construction safety management.

## Overview

Construction sites are highly dynamic environments where accidents can occur due to falls, struck-by incidents, caught-in/between hazards, electrical risks, equipment accidents, structural failures, chemical exposure, and confined space hazards.

This project uses Large Language Models (LLMs) and Vision-Language Models (VLMs) to analyze construction safety data from both text and images.

## Dataset

The study uses 28,575 construction-related OSHA accident reports collected from OSHA’s Integrated Management Information System (IMIS), covering accident records from 2000 to 2025.

Each report contains information such as:

- Event date
- Location
- NAICS code
- Worker age and sex
- Occupation
- Injury severity
- Investigation summary
- Accident cause

## Methodology

The framework has two main pipelines:

### 1. Textual Processing Pipeline

The textual pipeline uses an LLM to process OSHA accident reports. It extracts structured information from unstructured accident narratives and classifies each report into construction hazard categories.

The extracted fields include:

- Date of event
- Accident location
- Worker occupation
- Injury severity
- Accident cause
- Investigation summary
- Hazard category

The hazard taxonomy includes 43 subcategories grouped into major hazard families such as:

- Falls
- Struck-by incidents
- Caught-in/between hazards
- Electrical hazards
- Structure failures
- Vehicle and heavy equipment accidents
- Explosion and chemical exposure
- Confined space and oxygen deficiency
- Environmental and weather hazards

### 2. Visual Hazard Detection Pipeline

The visual pipeline uses a Vision-Language Model to analyze construction site images and identify visible hazards. The model reasons through each image using structured prompts and localizes high-risk objects using bounding boxes and annotations.

The visual pipeline can identify hazards such as:

- Suspended lifting chains
- Cutting saw operations
- Exposed electrical wiring
- Workers on sloped roofs
- Workers beneath heavy machinery
- Leaking chemical drums
- Collapsed structures
- Forklift instability
- Confined space hazards

## Models Used

The framework uses:

- GPT-4o-mini for text-based OSHA report analysis
- Qwen2.5-VL-3B-Instruct for construction site image understanding and hazard localization

## Results

The textual pipeline achieved 89% accuracy on a manually labeled test set. It successfully extracted key accident details and classified incidents using a 43-category hazard taxonomy.

The visual pipeline qualitatively demonstrated the ability to identify and localize high-risk construction hazards in site images using bounding boxes and hazard labels.

## Key Contributions

- Developed a two-pipeline multimodal AI framework for construction safety analysis
- Processed 28,575 OSHA construction accident reports
- Extracted structured safety information from unstructured accident narratives
- Classified accidents into detailed construction hazard categories
- Used a vision-language model to identify and localize hazards in construction site images
- Demonstrated how LLMs and VLMs can support construction safety management without fine-tuning

## Applications

This framework can help:

- Analyze large volumes of OSHA accident reports
- Identify common construction hazard patterns
- Support safety training and risk assessment
- Assist construction site safety inspection
- Improve accident prevention strategies
- Reduce manual review effort in safety analysis

## Keywords

Multimodal AI, Construction Safety, OSHA Accident Reports, Large Language Models, Vision-Language Models, Hazard Detection, Safety Management, Accident Analysis
