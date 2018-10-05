# Scrublet
**S**ingle-**C**ell **R**emover of Do**ublet**s  
  
Python code for identifying doublets in single-cell RNA-seq data. For details and validation of the method, see our preprint on [bioRxiv](https://www.biorxiv.org/content/early/2018/07/09/357368).


Given a raw counts matrix `E`, with cells as rows and genes as columns, you can calculate a doublet score for each cell with the following command: 
```python
import scrublet as scr
scrublet_results = scr.compute_doublet_scores(E)
doublet_scores = scrublet_results['doublet_scores_observed_cells']
```

There are a number of optional parameters that can have major effects on the quality of results. For a typical workflow, including interpretation of predicted doublet scores, see the example [ipython notebook](./examples/10X_PBMC-8k_example.ipynb).

We are also working on a [scanpy](https://github.com/theislab/scanpy) implementation. See https://github.com/swolock/scanpy for a fork implementing Scrublet and the example [here](./examples/10X_PBMC-8k_scanpy_example.ipynb).

#### To install:
```bash
git clone https://github.com/AllonKleinLab/scrublet.git
cd scrublet
pip install -r requirements.txt
pip install --upgrade .
```
#### Other doublet detection tools:
[DoubletFinder](https://github.com/chris-mcginnis-ucsf/DoubletFinder)  
[DoubletDecon](https://github.com/EDePasquale/DoubletDecon)  
[DoubletDetection](https://github.com/JonathanShor/DoubletDetection)
