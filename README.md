# Repository for "Fine-tuning protein language models boosts predictions across diverse tasks"

This repo contains all data used and generated during [this work](https://doi.org/10.1101/2023.12.13.571462).
We also provide Notebooks to reproduce our work, inlcuding examples.

- **[Embedding](notebooks/embedding)** contains notebooks to generate embeddings and train embeddings based predictors
- **[Finetuning](notebooks/finetune)** contains notebooks to finetune all protein language models used in our work 
- **[data](data/)** contains all data for figures in the main manuscript
- **[SOM data](SOM%20data)** contains all data for figures and tables in the Supplementary Online Material
- **training_logs.zip** contains the raw training history logging files our analysis is based on.
- **training data.zip** contains all training datasets used for this work. Each dataset consists of a training, validation, and test set. When using those data, please quote and consult the authors of the original data sets. But we recommend using the original data sources (linked below) as data available here will not be kept updated and mainly serves reproduction purposes.
  - GFP and stability:  https://github.com/songlab-cal/tape
  - AAV, GB1, Meltome and secondary structure: https://github.com/J-SNACKKB/FLIP
  - Subcellular Location: https://github.com/HannesStark/protein-localization
  - Disorder: https://github.com/DagmarIlz/SETH

**License**
   
   This data repository is released under terms of the [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).
