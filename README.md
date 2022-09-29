# Mutation Stability Data

Data for mutation effects on protein stability.  
In molecular biology, we call an amino acid in a protein sequence as a residue.

For `train.csv` and `test.csv`:  
`PDB`: PDB ID code, get widetype 3D structure from `https://files.rcsb.org/download/{pdb_id}.pdb`.  
`wildtype`: Wildtype amino acid.  
`position`: Resiude number of mutation in `sequence`.  
`mutation`: Changed amino acid in `mutant_seq`.  
`ddG`: Experimentally measured ∆∆G(folding), positive means more stable.  
`sequence`: Wildtype protein sequence.  
`mutant_seq`: Mutated protein sequence.  

For `tm.csv`:
`PDB`: PDB ID code, get widetype 3D structure from `https://files.rcsb.org/download/{pdb_id}.pdb`.  
`WT`: Wildtype amino acid.  
`position`: Resiude number of mutation in `sequence`.  
`MUT`: Changed amino acid in `mutant_seq`.  
`dTm`: Experimentally measured ∆T(melting), positive means more stable.  
`sequence`: Wildtype protein sequence.  
`mutant_seq`: Mutated protein sequence.  

# To predict mutation ∆∆G

[DDGscan](https://github.com/JinyuanSun/DDGScan)