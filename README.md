# Mutation Stability Data

Data for mutation effects on protein stability.  
In molecular biology, we call an amino acid in a protein sequence a residue.

## V1 data

These data were collected initially for my degree thesis research, which aimed to build a model for ∆∆G prediction from **Single Sequence** because at that time we did not have the AlphaFold2. Now I already gave up that project and changed my thesis from pure dry-lab to some "real" protein design project, and developed [DDGScan](https://github.com/JinyuanSun/DDGScan) by the way.

For `train.csv` and `test.csv`:  
`PDB`: PDB ID code, get widetype 3D structure from `https://files.rcsb.org/download/{pdb_id}.pdb`.  
`wildtype`: Wildtype amino acid.  
`position`: Residue number of mutation in `sequence`.  
`mutation`: Changed amino acid in `mutant_seq`.  
`ddG`: Experimentally measured ∆∆G(folding), positive means more stable.  
`sequence`: Wildtype protein sequence.  
`mutant_seq`: Mutated protein sequence.  

For `tm.csv`:  
`PDB`: PDB ID code, get widetype 3D structure from `https://files.rcsb.org/download/{pdb_id}.pdb`.  
`WT`: Wildtype amino acid.  
`position`: Residue number of mutation in `sequence`.  
`MUT`: Changed amino acid in `mutant_seq`.  
`dTm`: Experimentally measured ∆T(melting), positive means more stable.  
`sequence`: Wildtype protein sequence.  
`mutant_seq`: Mutated protein sequence.  

## V2 data

The V1 data was first released for kaggle competition [novozymes-enzyme-stability-prediction](https://www.kaggle.com/competitions/novozymes-enzyme-stability-prediction/overview), I cleaned and updated these data to this version, hope this will be helpful.

`pdb`: PDB ID code, get widetype 3D structure from `https://files.rcsb.org/download/{pdb_id}.pdb`.  
`wildtype`: Wildtype amino acid.  
`pdb_resseq`: Auth. Resseq number in the 6th col in a pdb file. **Not always starts from 1!**  
`seq_index`: Index in the seq string where a single mutation happens starts from 0.  
`mutation`: Changed amino acid in `mut_seq`.  
`wt_seq`:  Wildtype protein sequence.  
`mut_seq`:   Wildtype protein sequence.  
`ddG`: Experimentally measured ∆∆G(folding), positive means more stable.  
`group`: For K-fold CV. The `test.csv` does not have this.

## To predict mutation ∆∆G

A tool designed for enzyme stability prediction: [DDGscan](https://github.com/JinyuanSun/DDGScan)