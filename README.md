# structbio_scratch

This is a repository of structural bioinformatics workflows, designed for tasks related to topics such as structure-based drug design, molecular dynamics simulation setup and analysis.

The workflows include Python scripts which can be run from the Linux terminal. 

Please note that although the workflows are tested prior to their deposition here, they have not been designed with end users in mind. We only provide these for convenience to those who intend to perform similar tasks for their own projects. 

## List of workflows:

### dss.py
A parallelized workflow that calls DogSiteScorer 2 executable on snapshots obtained from a biomolecular simulation trajectory (no solvent or ions, just protein atoms).

DogSiteScorer 2 must be available from the command line. Note that you need license from BioSolveIT to use DoGSiteScorer. For more information, please visit <a href="https://www.biosolveit.de">BioSolveIT website</a>

### dss_analysis.py
A workflow that parses binding pockets predicted by DoGSiteScorer 2 from a biomolecular simulation trajectory/structural ensemble, and generates a clustermap showing residues forming different pockets on protein surface. The workflow uses the pocket definition files found in the output folder generated by dss.py.

This clustermap provides a visualization of potential druggable binding pockets and their persistence within the content of native state dynamics of the target protein. This may be useful for selection of potentially allosteric or cryptic binding pockets on protein structures.

### md_traj_analysis.py
**in progress**

### pandora.py
**in progress**

### frustratometer.py
**in progress**

### smina_screen.py
A parallelized workflow that takes an SDF file containing potential ligand molecules, a PDB file including pocket amino acids, and a PDB file containing receptor structures as input, and runs molecular docking simulations using smina. The results are returned in a single SDF file containing binding poses, and a data frame containing docking scores.

### pm_screen.py
A parallelized workflow that takes a list of gene names as input, retrieves PDB structures and AlphaFold2 models of each protein encoded by these genes, detects binding pockets using DoGSiteScorer 2, and computes similarities between these binding pockets using PocketMatch. 

DoGSiteScorer 2 and PocketMatch must be available from the command line. Note that you need license from BioSolveIT to use DoGSiteScorer. For more information, please visit <a href="https://www.biosolveit.de">BioSolveIT website</a>.

## How to use the workflows?

Clone the repository, open the file using Jupyter Notebook/JupyterLab or your favorite IDE (e.g. VSCode), install any dependencies required (using either pip or conda), modify the code as needed.

## Questions and comments

Please reach out to me (Onur Serçinoğlu) in case you have any questions or comments regarding these workflows. 
