Important Notes:
----------------

1. **For easy setup of a conda environment to run the notebooks you can use the finetuning.yml File provided in this folder**

    Check here for [setting up env from a yml File](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)
   
2. **For detailed examples, check the information inside the notebooks**

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

4. **Parameter efficient finetuing utilizes Huggingface [PEFT](https://huggingface.co/docs/peft/index)**
    - LoRA finetuing is used as default setting  
    - we provide an option to finetune entire models (we recommend this for models smaller than ESM2 650M)
    - other adapters availabe from Huggingface [PEFT](https://huggingface.co/docs/peft/index) can be easily plugged in

5. **Advice for memory efficient use**
    - always use mixed precision training 
    - if GPU memory overflow occurs, reduce batch size to 1 and simulated the desired batch size using gradient accumulation
    - if GPU memory still overflows, enable deepspeed to utilize cpu offloading
    - if GPU memory still overflows, remove(or truncate) long sequences

6. **Cite**

    If you use these notebooks in your work, please cite the authors of the original PLMs you are utilizing as well as [our work](https://doi.org/10.1101/2023.12.13.571462) during which they were created.

7. **License**
   
   This repository is released under terms of the [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).
