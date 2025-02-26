### Camformer
Predicting gene expression using millions of yeast promoters reveals *cis*-regulatory logic

**Problem**: Let $S = \{A,C,G,T,N\}^{110}$ denote a promoter sequence of length $110$. Here, $A$, $C$, $G$, $T$ are the four nucleotides and  $N$ represents an unknown nucleotide.  The gene expression prediction task is then to learn a mapping  $f: S \to \mathbb{R}$.

<div align="center">
    <img src="readme_figs/Fig1.jpg" alt="Graphical abstract" width="400">
</div>

**Data**: We use data from [DREAM Challenge](https://zenodo.org/records/7395397) consisting of 7 million random promoter sequences and the yellow fluorescent protein level. We then use the official test set from the challenge to evaluate our trained model(s).

**Model**: A residual convolutional neural network, strategically optimised using automated hyperparameter tuning.

<div align="center">
    <img src="readme_figs/Fig2.jpg" alt="Search for a model" width="400">
</div>

The figure above shows the structure of the original (large variant) model (16M parameters). There is an almost equally good model that has 90\% less parameters (1.4M). Please see the associated manuscript (preprint) for more details. 

**Assessment**: Predictive, comparative

<div align="center">
    <img src="readme_figs/Fig3.jpg" alt="Evaluating a trained model" width="400">
</div>

**Assessment**: Explanatory, Scientific discovery

<div align="center">
    <img src="readme_figs/Fig4.jpg" alt="Evaluating a trained model for explanatory assessment" width="400">
</div>


#### File information

Here are some details on what the purpose of each file is:

| File               | Purpose                                                                       |
|:-------------------| :-----------------------------------------------------------------------------|
| `gen_figs.ipynb`   | A notebook to show (re-generate) some figures in the manuscript.              |
| `train_rep.py`     | Program to train several replicates of a Camformer model using training data. |
| `score_rep.py`     | Program to test several replicates of a trained Camformer model on test data. |


#### Directory structure

| Directory           | Contents                                                                |
|:--------------------| :-----------------------------------------------------------------------|
|`analysis`           | Contains some basic analysis of results. Contents may be updated.       |
|`base`               | Contains core codebase, utility functions, auxiliary helper files etc.  |
|`manuscript_figures` | Contains data, script and figures present in the manuscript.            |
|`readme_figs`        | Images used to prepare this nice-looking README file.                   |
|`saved_models`       | Saved model weights and example code to run.                            |


#### References

Relevant resources and previous Camformer repositories.

1. Camformer repository (2022 version): [DREAM2022 Submission](https://github.com/FredrikSvenssonUK/DREAM2022_Camformers)
2. DREAM 2022 Challenge [Wiki Page](https://www.synapse.org/#!Synapse:syn28469146/wiki/617075)
3. Rafi et al., 2024: [Paper](https://doi.org/10.1038/s41587-024-02414-w) [Preprint](https://www.biorxiv.org/content/10.1101/2023.04.26.538471)
4. Rafi et al., 2024: [Data and Official Evaluation](https://zenodo.org/records/10633252) [GitHub](https://github.com/de-Boer-Lab/random-promoter-dream-challenge-2022)

