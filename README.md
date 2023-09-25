# Exploring how missense variant stability shapes protein functional data

### Abstract

Missense variants can greatly impact the normal function of a protein. However, some variants may cause loss of protein function by decreasing protein stability, and some may directly interfere with the protein functions (e.g., directly interrupt a catalytic reaction). Here, I work towards an automatic and generalised method to qualitatively measure the influence of stability change on variant fitness. 

In this study, I collected both DMS-measured variant fitness data and Rosetta-computed variant stability data for more than 135,000 missense variants. I systematically evaluate how variant stability correlates with fitness data on different amino acids and protein properties measured. I then leverage a cross-decomposition method, Canonical Partial Least Squares (PLS), to distinguish protein residues with different scales of fitness–stability association. Further investigation indicates that this method can be used to discover protein functional sites and explain the mechanisms of loss-of-function variants.

### Setup & usage

1. Create a virtual environment with Python 3.8.
2. Install Jupyter Notebook and other required pacakges according to `requirements.txt`
3. Follow the code and instructions in the notebook (`./jupyter_code/Explore_DMS_stability_association.ipynb`).

### Data content
* `dms_feature_data.csv` contains collected DMS data, together with predicted GEMME scores, Rosetta _ΔΔG_, normalised B-factors, and surface accessibility values.
* `dms_info.csv` contains data information of the DMS experiments as well as categorised DMS assay types.
* `active_sites.csv` contains enzyme active sites stored in M-CSA which was filtered to only include the enzymes (and regions) where I also have DMS data.