> Most species have more than one versions of the reference genome. Please find out:  

* The name and time of the latest version for Human, Mouse and E Coli.  
  - Human: GRCh38/hg38 (Dez 2013) 
  - Mouse: GRCm39/mm39 (Jun 2020)
  - E. Coli: ASM584v2 (Sep 2013)
  
* The name and time of the first version for Human, Mouse and E Coli.
  - Human: NCBI34/hg16 (July 2003)
  - Mouse: NCBI35/mm7 (Aug 2005)
  - E. Coli: ASM584v1 (Jun 2004)


* How many reference genomes were released in total for Human, Mouse, and E Coli.
  - Human: 5
  - Mouse: 5
  - E. Coli: 2

> What do you think of the difference between genome versions?

- Find out the difference in chromosome length between the latest patch of
hg38 and the last patch of hg19. 

  - hg38 total sequence length: 3,099,706,404  
  - hg19 total sequence length: 3,101,788,170  
  - difference in chromosome length btw hg38 and hg19: 2'081'766 bp  

- With your favorite gene, find out its position in hg38 and hg18.

  - hg38: OCA2 at chr15:27754875-28099315  
  - hg18: OCA2 at chr15:25673616-26018056  

> The USCS Genome Browser

* Show gene TP53 in the genome browser.
* Where is this gene? (chromosome, cytoband, and exact start and end positions)
  - Chromosome 17, cytoband 17p13.1, from chr17:7,668,421 to chr7:7,687,490, length 19,070 bp.  
  
* How many isoforms does it have?
  - 9 isoforms  

* How many exons does it have?
  - 12 exons (7 coding exons)  

* What the size of its longest exon? (roughly)
  - 1'300 bp  

* Find the three closest genes in upstream and downstream, respectively.
  - upstream: ATP1B2, SHBG, SAT2
  - downstream: WRAP53, DNAH2, EFNB3  

> TP53

* Switch to hg19 and find TP53.
* What is the start and end positions?
  - from chr17:7,571,720 to ch17:7,590,868, length: 19149 bp 
    
* Switch to zebrafish, can you find TP53?
  - yes on Chromsome 5, from chr5:24,086,227 to chr5:24,097,799, length: 11,573 bp  
  
* Switch to Fruitfly, can you find TP53?
  - I found on chromosome 2R a TP53 homeolog, from chr2R:11,983,429 to chr2R:11,984,899, length: 1,471 bp  

> Liftover with USCS Genome Browser  

* Down-lift: TP53 from hg38 to hg19
  - chr17:7,668,421-7,687,490 to chr17:7571739-7590808

* Up-lift: TP53 from hg19 to hg38
  - chr17:7,571,720-7,590,868 to chr17:7668402-7687550
 
* Cross-species-lift: TP53 from human to mouse
  - chr17:7,668,421-7,687,490 to chr11:69471228-69482695

* Multi-step-lift: TP53 from hg38 to hg18
  - chr17:7,668,421-7,687,490 to chr17:7571739-7590808 to chr17:7512464-7531533

> BED file liftover

* Liftover multiple positions with a BED file. Lift a larger range and interpret the result.
  - tried to liftover example.bed: works for 74 records, but failed to liftover 24 records.  
  
* Limitations of the liftover.
  - When liftover larger ranges it can lead to several errors as:  
    - #Deleted in new
    - #Partially deleted in new 
    - #Split in new
  - The mapping is often not straightforward, specially when a region has been deleted/added, over gaps or if SNVs with mutliple coordinates are present in target/original genome.      
  - If positions are too distanced, they may be seperated and cannot e mapped properly to another assembly.

