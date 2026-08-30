# Enzyme_comparative_tool
A Python-based tool for preliminary comparative screening between enzymes based on two main characteristics: hydrophobicity and threonine presence
The basic comparative analysis of candidate enzymes is based on the possibility of manufacturing high-purity biosurfactants.
The Python script is based on an automated digital screening tool that retrieves UniProt data for structural traits that match the predetermined requirements of the enzyme of interest.
The screening provides an initial indication of characteristics potentially relevant to enzyme stability and industrial application, allowing less suitable candidates to be deprioritised before more detailed structural analysis and experimental validation.

This project currently focuses on two simple sequence-composition metrics sourced through UniProt:
### Hydrophobic Residue Content
By calculating the percentage of hydrophobic amino acids, the script compares the overall hydrophobic residue composition of each candidate enzyme. Hydrophobic residues are among the factors involved in protein folding and stability through hydrophobic interactions. The script allows a rough comparison of physicochemical compositions before structural or local hydropathy analysis is performed to identify the hydrophobic core and membrane-binding region; it does not directly identify these regions.

### Threonine Content
Threonine is a polar amino acid with a hydroxyl-containing side chain capable of participating in hydrogen bonding, which can contribute to protein structure and stability depending on its position within the protein. 
Threonine residues may also serve as sites for O-linked glycosylation in organisms that undergo this modification. 
The script calculates threonine content as a simple compositional metric. 
Higher threonine content may indicate differences in hydrogen-bonding potential, but further structural analysis is required to determine its actual contribution to protein stability, glycosylation, or secretion.

## Workflow

1. Define candidate UniProt accession IDs.
2. Connect to the UniProt REST API.
3. Retrieve protein records in JSON format.
4. Extract:
   - UniProt accession
   - organism
   - primary amino-acid sequence
   - sequence length
5. Calculate threonine residue content.
6. Calculate hydrophobic residue content.
7. Compare results between candidate proteins.
8. Identify candidates for further computational or experimental analysis.

## Tools used
- Python
- UniProt REST API
- JSON
- urllib
- SSL / Certifi
- Jupyter Notebook

 ## Current Limitations
This project is intended as a preliminary sequence-screening exercise and does not predict industrial enzyme performance.

Whole-sequence amino-acid composition cannot determine protein tertiary structure, thermal stability, membrane association, enzyme activity,
substrate specificity or biosurfactant production.
Experimental validation would therefore be required before drawing conclusions about industrial suitability.
