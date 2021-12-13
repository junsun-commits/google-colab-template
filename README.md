## Trinity 
This is the presentation material _(pdf & ipynb)_ for Trinity tool based on the published manuscript;

Grabherr, Manfred G et al. “Full-length transcriptome assembly from RNA-Seq data without a reference genome.” _Nature biotechnology_ 29-7(2011): 644-52.

Briefly, Trinity is an RNA-Seq de novo transcriptome assembly tool that works in three main stages;

**0. Jellyfish:**
Extracts and counts _k-mers_ (K=25) from reads.

**1. Inchworm:**
Assembles initial contigs by "greedily" extending sequences with most abundant _k-mers_.

**2. Chrysalis:**
Clusters overlapping Inchworm contigs builds de Bruijn graphs for each cluster, partitions reads between clusters.

**3. Butterfly:**
Resolves alternatively spliced and paralogous transcripts independently for each cluster (in parallel).

_Contact: Catherine Apio (2019-20240@snu.ac.kr)_.
