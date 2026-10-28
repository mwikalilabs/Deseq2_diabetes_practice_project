## Deseq2_diabetes_practice_project
## Practising the differential expression workflow: type 2 diabetes vs healthy pancreatic islets

**This is a practice project.** I built it to get hands-on experience with RNA-seq differential expression workflow. It is a learning exercise, not original research, and nothing here should be read as a scientific finding.

### Dataset

- Source: Expression Atlas, experiment E-MTAB-5060 (whole-islet RNA-seq, human pancreas, type 2 diabetes vs healthy)
- Files used: raw counts and the experiment design file 
- 7 samples (4 type 2 diabetes, 3 normal)

### Tools

Python, Jupyter Notebook, pandas, numpy, seaborn, matplotlib, scikit-learn, PyDESeq2 (0.5.4)

### Workflow practised

1. **Load and align** the counts and sample metadata, and check that every sample matches its label.
2. **Check the study design** for confounders (age, BMI, sex).
3. **Filter** low-expressed genes before testing.
4. **Explore the data:** library sizes, CPM, log2 transformation, sample boxplots.
5. **PCA** coloured by disease, age and sex, to look for structure and outliers.
6. **Differential expression** with PyDESeq2, with normal as the reference level and multiple-testing correction (Benjamini-Hochberg adjusted p-values).
7. **Visualized** the results with a volcano plot.
8. **Map gene IDs to gene names** and read about what some of the top genes do.

### Notes on the data

- Only 7 samples, so statistical power is low.
- Age differs between the groups (the type 2 diabetes samples are older), so age is confounded with disease.(The analysis in this notebook didn't adjust for it.)
- One normal sample is an outlier on the PCA plot.(It was kept in the analysis.)
- Whole islets contain a mixture of cell types.

Because of these points, this analysis is for learning the workflow and not for drawing conclusions about type 2 diabetes.

### Repository contents

- Dseq2_diabetes_practice_project.ipynb: for the analysis
- Data: E-MTAB-5060-experiment-design.tsv ,E-MTAB-5060-raw-counts.tsv
