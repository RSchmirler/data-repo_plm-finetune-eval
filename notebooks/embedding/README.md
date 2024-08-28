Important Notes:
----------------

1. **Environment**

    For the embedding notebooks you need the following packages installed (our versions are given insight the notebooks):
	- [Pytorch](https://pytorch.org/get-started/locally/)
	- [Tensorflow](https://www.tensorflow.org/install/pip)
	- [Transformers](https://huggingface.co/docs/transformers/de/installation)
	- [Pandas](https://pandas.pydata.org/docs/getting_started/install.html)

    You can also use the [finetune.yml file](../finetune/) to [set up a conda environment](https://conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#creating-an-environment-from-an-environment-yml-file)
   
2. **Example - GB1 prediction task using ESM2 8M**
    - First, run the GB1 example cell in the [Embedding_Generation_GPU](./Embedding_Generation_GPU.ipynb) notebook to compute the embeddings.
    - Second, train a small prediction head and validate the model on the test set using the [Embedding_Predictor_Training](./Embedding_Predictor_Training.ipynb) notebook.	

3. **To generate embeddings for your own datasets, follow the examples in the [Embedding_Generation_GPU](./Embedding_Generation_GPU.ipynb) notebook**

4. **[Embedding_Predictor_Training](./Embedding_Predictor_Training.ipynb) is used for both, per protein and per residue prediction tasks**

5. **These notebooks support the following pretrained PLMs**

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

6. **Cite**

    If you use these notebooks in your work, please cite the authors of the original PLMs you are utilizing as well as [our work](https://www.nature.com/articles/s41467-024-51844-2) during which they were created.

7. **License**
   
   The data in this repository is released under terms of the [CC-BY-4.0](https://creativecommons.org/licenses/by/4.0/).

   The source code in this repository is licensed under the MIT license, which you can find in the MIT-LICENSE.txt file.
