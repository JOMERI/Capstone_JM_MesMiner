## Capstone_project_MesMiner

The 2019 coronavirus pandemic outbreak has been an unprecedented health risk event caused by a severe acute respiratory syndrome. Global effort has been focused to finding a functional vaccine as well as novel treatment to reduce the severity of ICU patients. The scientific community has been researching insensitivity to understand the mechanism of COVID-19 with the immune response. By understanding COVID-19 better drug development and drug repurposing approaches could be performed rapidly and more efficiently. The major aim of this project is to develop a text mining platform from the abstracts of each papers published covering COVID-19 related research to create a database with all the novel biological outcomes. The focus is to identify and normalise gene and drug mentions from the paper abstracts. 

This would facilitate the transfer of the new dataset into current interactome databases with the aim to facilitate analysis and ease the finding of new potential interactions that are not currently been investigated. At this stage, only abstracts were analysed, future steps will include the analysis of the whole manuscript and to extract the quantitative data from each publication. Scispacy, an natural processing language (NLP) library was used to identify biological terms, gene, drugs, and gene regulations. By combing this with molecular biology datasets a fine curated dataset with the most frequent gene and drugs mentioned in the COVID-19 dataset can be developed. This method combined with machine learning pipelines could represent a great tool to accelerate translational research.

This project is divided in four Jupiter notebooks with annotations as a guide:

•	Data processing

•	Gene and drugs references

•	Scispacy

•	Visualisation

Notebooks contain annotations

A running version of the visualisation can be foud here:
https://www.kaggle.com/josemeseguer/mes-miner-text-mining-for-genes-drugs-cord-19

The first notebook covers the data processing from the CORD-19 dataset (https://www.semanticscholar.org/cord19). The major aim of this notebook is to clean the data, create a tag of publication type (preprint/peer-reviewed) and to lemmatise the abstract in preparation to the NLP. This notebook also includes a visualisation of the type of publication over time. The data used for this project was obtained from the metadata.csv file from the CORD-19 2020-08-05 release
 (https://ai2-semanticscholar-cord-19.s3-us-west-2.amazonaws.com/historical_releases.html) 
 
![publications_years](https://user-images.githubusercontent.com/58293705/90866989-943a5980-e38c-11ea-9e50-8429461c8a11.png)

Gene and drugs references notebook focuses in creating a dictionary with a standardised nomenclature for a given gene or drug. It would be possible then to search for name variations of a given term and unify its nomenclature for frequency counts. The drug database was downloaded via Drugbank (https://www.drugbank.ca/releases/latest) whereas the gene database was downloaded from SNAP (https://snap.stanford.edu/biodata/datasets/10022/10022-G-SynMiner.html)

Next, the Scispacy notebook will perform the NLP from each abstract of the dataset and identify biological related entities, genes and drugs named in a given abstract. In addition, a basic gene regulation identification was performed by looking for common terms used to describe gene regulation in the surrounding text of an identified gene. This process creates a new processed dataset for many potential downstream applications. 

Finally, the visualisation notebook allows the user to visualise and export the top genes, drugs and gene regulation. In addition, this notebook allows a custom search of the dataset to search for specific biological terms or type of publication prior finding the top entities.

![Gene_drugs_visualization](https://user-images.githubusercontent.com/58293705/90867022-a916ed00-e38c-11ea-8eec-d0d5a8159b66.png)
