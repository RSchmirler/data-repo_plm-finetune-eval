Important Notes:
----------------

1. **For easy setup of a conda environment to run the notebooks you can use the finetune.yml File provided in this folder**

    Check here for [setting up env from a yml File](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)
   
2. **For detailed examples, check the information inside the notebooks**
    - [Finetuning_per_protein](./Finetuning_per_protein.ipynb) for predictions on protein level (both classification and regression) <a href="https://colab.research.google.com/drive/12AwUjtnTg0NurKvIeqR5VL6uMtm7T0pT" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Colab-Version"/></a>
    - [Finetuning_per_residue_classification](./Finetuning_per_residue_classification.ipynb) for classification of individual residues <a href="https://colab.research.google.com/drive/1-2H37AHy_hchhgEETJZ53GaM-P4goDxV" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open Colab-Version"/></a>
    - [Finetuning_per_residue_regression](./Finetuning_per_residue_regression.ipynb) for regression tasks on residue level <a href="https://colab.research.google.com/drive/1M-MEouCZVVuILJLLB8drVKiaEoQ7AVOd" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a>

3. **These notebooks support the following pretrained PLMs**

| Model | Huggingface Checkpoints |
| ----------- | ----------- |
| [ESM2 8M](https://www.science.org/doi/full/10.1126/science.ade2574) | "facebook/esm2_t6_8M_UR50D" |
| [ESM2 35M](https://www.science.org/doi/full/10.1126/science.ade2574) | "facebook/esm2_t12_35M_UR50D" |
| [ESM2 150M](https://www.science.org/doi/full/10.1126/science.ade2574) | "facebook/esm2_t30_150M_UR50D" |
| [ESM2 650M](https://www.science.org/doi/full/10.1126/science.ade2574) | "facebook/esm2_t33_650M_UR50D" |
| [ESM2 3B](https://www.science.org/doi/full/10.1126/science.ade2574) | "facebook/esm2_t36_3B_UR50D" |
| [Ankh-base](https://arxiv.org/abs/2301.06568) | "ElnaggarLab/ankh-base" |
| [Ankh-large](https://arxiv.org/abs/2301.06568) | "ElnaggarLab/ankh-large" |
| [ProtT5](https://ieeexplore.ieee.org/document/9477085) | "Rostlab/prot_t5_xl_uniref50" |
| [ProstT5](https://www.biorxiv.org/content/10.1101/2023.07.23.550085v2) | "Rostlab/ProstT5" |

4. **Parameter efficient finetuning utilizes Huggingface [PEFT](https://huggingface.co/docs/peft/index)**
    - LoRA finetuning is used as default setting  
    - we provide an option to finetune entire models (we recommend this for models smaller than ESM2 650M)
    - other adapters availabe from Huggingface [PEFT](https://huggingface.co/docs/peft/index) can be easily plugged in

5. **Advice for memory efficient use**
    - always use mixed precision training 
    - if GPU memory overflow occurs, reduce batch size to 1 and simulated the desired batch size using gradient accumulation
    - if GPU memory still overflows, enable DeepSpeed to utilize CPU offloading
    - if GPU memory still overflows, remove(or truncate) long sequences

6. **Cite**

    If you use these notebooks in your work, please cite the authors of the original PLMs you are utilizing as well as [our work](https://www.nature.com/articles/s41467-024-51844-2) during which they were created.

7. **License**
   
   The data in this repository is released under terms of the [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).

   The source code in this repository is licensed under the MIT license, which you can find in the MIT-LICENSE.txt file.
