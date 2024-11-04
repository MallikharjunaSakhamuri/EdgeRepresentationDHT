
# EdgeRepresentationDHT

This repository contains the code and data for the research paper:

"Understanding and Classification of Innate Immune Response through Edge Representation Learning with Dual Hypergraph Transformation"

Authors: Mallikharjuna Rao Sakhamuri, Shagufta Henna, Leo Creedon, Kevin Meehan  
Affiliations: Atlantic Technological University, Ireland

## Overview

In this study, we propose a novel graph-based neural network approach for modeling peptide-human leukocyte antigen (HLA) interactions. Traditional machine learning approaches often overlook the critical correlations between amino acids, limiting the accurate prediction of binding affinities essential for advancing immunotherapies and understanding T cell responses.

Our method, Edge Representation Learning with Dual Hypergraph Transformation (DHT), leverages graph-based models to encode binding affinity interactions between HLA and peptides, incorporating relevant physicochemical properties. By applying a dual hypergraph transformation, we reinterpret nodes as edges and vice versa, generating an alternative graph representation that enhances our model's ability to capture complex relationships. This approach demonstrates significant improvements in classification accuracy on COVID-19 and dengue datasets, focusing on the underlying dynamics of binding affinities.

## Repository Contents

- `edgerepresentationdht.py`: Contains the main implementation of the Edge Representation Learning model with Dual Hypergraph Transformation (DHT). This script defines the model, data processing steps, and the training pipeline used in our study.
- `Data/`: Contains the dataset files used for the experiments in the paper. These files include data on peptide-HLA interactions relevant to COVID-19 and dengue, organized and preprocessed for direct use with the model.
  - `Datafiles.txt`: Describes the contents of each data file, including the purpose and format. Please refer to this file for detailed information about each dataset.
  
## Data Files

The `Data/` folder includes the following files (see `Datafiles.txt` for more details):

- `after_pca.txt`: PCA-transformed dataset for dimensionality reduction.
- `balanced_high_positive_negative_immunogenicity.csv`: Balanced dataset for model training.
- `covid_predicted_result.csv`: Predicted results for COVID-19 antigens.
- `deephlapan_result_cell.csv`: Comparison results from the DeepHLApan model.
- `dengue_test.csv`: Dengue-related test dataset.
- `edges_values.csv`: Edge values representing HLA-peptide relationships.
- `hla2paratopeTable_aligned.txt`: Aligned HLA paratope data.
- `ori_test_cells.csv`: Original test cell data.
- `remove0123.csv`: Data with specific outliers removed.
- `remove0123_sample100.csv`: Sample subset for testing.
- `remove0123_test.csv`: Test dataset with outliers removed.
- `sars_cov_2_result.csv`: Predicted results for SARS-CoV-2 antigens.

## Requirements

To run the code, you will need the following Python packages:

- `numpy`
- `scipy`
- `pandas`
- `networkx`
- `torch` (for PyTorch, the deep learning framework)

You can install these dependencies via pip:

```bash
pip install numpy scipy pandas networkx torch
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/EdgeRepresentationDHT.git
   cd EdgeRepresentationDHT
   ```

2. Run the Model:

   - Ensure the required data files are present in the `Data` directory.
   - Execute `edgerepresentationdht.py` to start training and testing the model on the included datasets:

     ```bash
     python edgerepresentationdht.py
     ```

3. Modifying Data:

   - You can replace or add new data files to the `Data/` directory if you wish to test the model with other datasets.
   - Ensure that any new data follows the expected format as described in `Datafiles.txt`.

## Results

The results demonstrate that our approach, leveraging dual hypergraph transformation, can accurately predict binding affinities for immune response modeling. Detailed performance metrics and comparison with traditional approaches are provided in the paper.

## Citation

If you use this code in your research, please cite our paper:

```bibtex
@article{sakhamuri2023edgerepresentationdht,
  title={Understanding and Classification of Innate Immune Response through Edge Representation Learning with Dual Hypergraph Transformation},
  author={Sakhamuri, Mallikharjuna Rao and Henna, Shagufta and Creedon, Leo and Meehan, Kevin},
  journal={},
  year={2024}
}
```

## License

This repository is released under the [MIT License](LICENSE). Please see the LICENSE file for more information.

---
