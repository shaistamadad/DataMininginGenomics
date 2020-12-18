Instructions
Querying the database and Analyzing the data. 

We will now mine RNA-seq data to learn more about these cancer genes. In order to avoid putting too much stress on the UCSC database,  some of the tables have been copied to a server called orion.bio.nyu.edu. I used  the MySQL access to connect to Orion and answered the following questions. 


1. For all the genes in the "cancerGenes.names.txt file"*,  identify their name, name2, chromosome, strand, transcription start and transcription end coordinates. This information is available in the table refGene. Save this dataframe as refGenesCoor 

** note, the name field is the refgene name, however the names provided in the files are found in the name2 field of the refGene table. 

** note that there will be several rows that contain a match to some genes. This is because there are multiple transcripts from the same locus. In such cases ONLY keep the first row. 

 

Store this dataframe refGenesCoor in your sqlite database called hg19.sqlite 

2. For each gene, determine the number of reads that map to the different tissues. The sequence reads are stored in tables that begin with “burge”. Each row in a given table is one read and it contains the coordinates of the match. So you can simply count the number of rows that are returned when asking for all reads that match within the coordinates of a gene.

Use the following tissues/tables: 

a. burgeRnaSeqGemMapperAlignBrain 

b. burgeRnaSeqGemMapperAlignBreast 

c. burgeRnaSeqGemMapperAlignColon 

d. burgeRnaSeqGemMapperAlignHeart 

e. burgeRnaSeqGemMapperAlignLiver 

f. burgeRnaSeqGemMapperAlignLymphNode 

g. burgeRnaSeqGemMapperAlignSkelMuscle 

h. burgeRnaSeqGemMapperAlignTestes 

Save this information in a data frame where each row is the gene and each column is a different tissue type. Save this dataframe as GeneRNAseq and add it to your hg19.sqlite database as a table. 

3. A common way of normalizing RNA-seq data is to calculate TPM (Transcripts per million). To obtain this value : 

Divide each read count in GeneRNAseq with its corresponding transcript size. To calculate the transcript size you will have to add size of all the exons for the given gene. In refgene you are provided with exonStarts and exonEnds, simply subtract the two and add one for each exon.

Now divide each value by the column sum of the corresponding column and multiply by 1 million.

The link below has a video that explains TPM and other types of normalization for your reference: https://www.rna-seqblog.com/rpkm-fpkm-and-tpm-clearly-explained/



 

4. Calculate the average gene expression for each gene. Which gene has the 

highest average expression across all samples? 

a. (Highest row mean) 

5. For this gene(with the highest gene expression), create a barplot showing the level of expression for each sample. 