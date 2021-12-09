# STAR : Spliced Transcripts Alignment to a Reference.
STAR is a RNA-seq aligner that improves sensitivity and precision, high mapping speed!

## Current branches
- STAR

## Installation
Use these two reference [Author manuscript](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4631051/) & [STAR manual](https://physiology.med.cornell.edu/faculty/skrabanek/lab/angsd/lecture_notes/STARmanual.pdf) to install STAR.

```bash
wget https://github.com/alexdobin/STAR/archive/2.7.9a.tar.gz
tar -xzf 2.7.9a.tar.gz
cd STAR-2.7.9a/source

sudo apt-get update
sudo apt-get install g++
sudo apt-get install make
make STAR
chmod +x STAR
```

## Usage

```bash
#If you want to check the option !

./STAR --help

#basic protocol - 1) generating genome indices

STAR  \
--runThreadN 12 --runMode genomeGenerate --genomeDir ./ --genomeSAindexNbases 12 \
--genomeFastaFiles ./Mus_musculus.GRCm39.dna.chromosome.1.fa

# - 2) align transcript to a reference

STAR --runThreadN 12 --runMode alignReads  \
--genomeDir ../genome/ --sjdbGTFfile ../Homo_sapiens.GRCh38.79.gtf \
--sjdbOverhang 100 --readFilesIn ../ENCFF001RFH.fastq.gz  ../ENCFF001RFG.fastq.gz  \
--outSAMtype BAM SortedByCoordinate
```
Parameters used above example are suited for human.

## The Requirement of STAR
RAM : At least 10 * GenomeSize bytes. 
(ex) human genome of ~3 GigaBases will require ~30 GigaBytes of RAM. 32GB is recommended for human genome alignments.

Disk Space : sufficient free disk space (>100 GigaBytes) for storing output files.

(It is recommended to use a local computer or a server because the specification of Google Colaboratory does not meet the requirement written above.)

Also, STAR can be run on Unix, Linux or Mac OS X systems.
(If you want run STAR on Windows, you must install Windows Subsystem for Linux (WSL))

## Contributing
Pull requests are welcome. 
For major changes, please open an issue first to discuss what you would like to change.
Please make sure to update tests as appropriate.

## License
[STAR: ultrafast universal RNA-seq aligner](https://doi.org/10.1093/bioinformatics/bts635)
