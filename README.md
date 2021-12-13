# MAFFT
> Advanced Bioinformatics 1, Fall 2021<br>Seoul National University<br>by Daniel DW Kim

## Materials
This readme covers the content of [this notebook](Adv_BI_Fall_2021_MAFFT.ipynb). You can also refer to [these slides](Adv_BI_Fall_2021_MAFFT.pdf) for some background information.

## About MAFFT
MAFFT is a progressive alignment-based multiple sequence alignment program for biological sequences. MAFFT utilizes a [fast Fourier transform](https://en.wikipedia.org/wiki/Fast_Fourier_transform) algorithm to speed up the process of multiple alignment. 

* [MAFFT homepage](https://mafft.cbrc.jp/alignment/software/) <br>
* [Original paper (*NAR*)](https://academic.oup.com/nar/article/30/14/3059/2904316)
* [Version 7 paper (*MBE*)](https://academic.oup.com/mbe/article/30/4/772/1073398)

## Run MAFFT with Colab [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1KyKyKD2H_a60RIgFzDqVbRfKC3D_Gxo0?usp=sharing)
### Step by step guide
* Prepare a data by downloading the [FASTA file](rpb1.fa) on your working directory.
* Run **Install MAFFT** block to automatically install MAFFT on your local filesystem.
* Run FFT-NS-2 and FFT-NS-i algorithm on your data by sequentially running the blocks.
* Provide CLUSTAL format outputs and compare your results.

## Want some more fun?
Aligned results can be further visualized and analyzed by using external softwares specialized for phylogenetics.

* [MEGA X](https://www.megasoftware.net/)
* [ete toolkit](http://etetoolkit.org/)
* [iTOL](https://itol.embl.de/)
