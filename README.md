# MYLU_eQTL

This repository is associated with the manuscript "Impact of Putatively Beneficial Genomic Loci on Gene Expression in Little Brown Bats (Myotis lucifugus, Le Conte, 1831) Affected by White-Nose Syndrome"

In this manuscript we use an expression quantitative trait loci (eQTL) analysis to determine if genomic loci previously found by Gignoux-Wolfsohn et al, 2021 to be under selection due to WNS impact gene expression in the wing tissue of hibernating M. lucifugus.

149 wing biopsy samples were collected from hibernation sites in 5 states throughout the USA; New York, New Jersey, Kentucky, Michigan, and Vermont. 99 of these were from WNS infected hibernacula supporting bat colonies and 48 were from hibernacula in New York and Kentucky that had not been exposed to WNS at the time of collection.

We cut each biopsy in half, one half for DNA extraction and genotyping and one half for RNA extraction and edge-Seq.

For genotyping, we had custom molecular baits produced by arbor scientific targeting the SNPs found in Gignoux-Wolfsohn et al, 2021. These SNPs are referred to as the target SNPs in this repository and the sites are specified in the "Baits" folder.
In addition, we the baits covered the 1,000 bp flanks on either side of the target SNPs, hereby referred to as the target regions. These were included to test for functionality in SNPs that exist in linkage disequilibrium with the target SNPs.
Lastly, the baits included 1,000 sets of 1,000 bp regions randomly selected from throughout the genome in order to determine if any activity in the target regions was more than would be expected by chance.
Our bioinformatics pipeline for genotyping can be found in the DNA folder, in order of parts.

For gene expression, we created edge-seq mRNA libraries which save on sequencing costs while performing on par with full length RNA-seq for gene expression studies. 
Our bioinformatics pipeline for creating read tables can be found in the RNA folder.

The genotype file created from the DNA pipeline and the read count table generated from the RNA pipeline were then used in 2 separate eQTL analyses. The first considered only the target SNPs while the second included target region and random region SNPs.
The code for these analyses can be found in the eQTL folder.

Finally, we compared gene expression between samples collected from unexposed hibernacula and exposed hiberncula using a differential expression analysis. We also compared the values of principal component 1 between exposed and unexposed populations.
The code for these analyses can be found in the 
