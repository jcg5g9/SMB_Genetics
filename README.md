# Smallmouth_Bass_Genetics_R_Scripts

# Aim 1 - Population Structure Analysis
### File: NSMB_Microsats_STRUCTURE.Rmd

Purpose: I am assessing population structure of Smallmouth Bass and Spotted Bass in the Central Interior Highlands where the native ranges of the Northern and Neosho Smallmouth Bass meet. I am analyzing STRUCTURE at the population level (28 putative populations consisting of 43 collection sites). I am assessing population structure with three different sets of parameters within the external software program STRUCTURE: 1) "Default Parameters": parameters set to default in the program STRUCTURE and using delta K to infer best K, 2) "Wang Parameters": parameters recommended by Wang (2017) and using delta K to infer best K, and 3) "Puechmaille Inference": parameters set to default but using Puechmaille metrics to infer best K.

### Bayesian Parameters Used for all analyses:

#### Burn-in: 500,000
#### MCMC: 1,000,000
#### Reps: 10
#### All Samples: K = 1-15
#### Northern and Spotted Samples: K = 1-5
#### Neosho Samples: K = 1-10

### Data Used:

#### All microsatellite data: 766 Samples, 14 microsatellite loci

# Aim 2 - Genetic PCA (Multivariate PCA) Analysis
### File: NSMB_Microsats_GENETIC_PCA.Rmd

Purpose: I am assessing genetic differentiation between Spotted Bass and Smallmouth Bass, between Northern Smallmouth Bass and Neosho Smallmouth Bass, and also population structure among all Smallmouth Bass populations using Principal Components Analysis of my microsatellite data.

### Data Used:

#### All microsatellite data: 766 Samples, 14 microsatellite loci

# Aim 3 - Genetic Diversity Analysis
### File: NSMB_Microsats_GENETIC_DIVERSITY.Rmd

Purpose: I am assessing differences in genetic diversity between Northern Smallmouth Bass and Neosho Smallmouth Bass. I am specifically calculating five genetic diversity metrics (rarefied allelic richness, observed heterozygosity, expected heterozygosity, private allele frequency, and common allele frequency) at the level of collection site (43 total collection sites) across my Smallmouth Bass samples (N = 766 total samples). Allelic richness (AR) and private allele frequency (AP) were both calculated using the software program HP-RARE, which is not built into R. Values across sampling sites were manually imported into Excel, along with the calculations conducted for allelic richness, heterozygosity, and common allele frequency, which were then all separately imported into R for downstream analysis. I am then testing for differences in these metrics using linear mixed ANOVA models at the subspecies level. 

### Data Used:

#### All microsatellite data: 766 Samples, 14 microsatellite loci

# Aim 4 - Morphological Analysis
### File: NSMB_Microsats_MORPHOLOGY.Rmd

Purpose: I am assessing morphological differentiation between the Neosho Smallmouth Bass and Northern Smallmouth Bass where their ranges meet in the Central Interior Highlands. I am to assess overall divergence using multivariate methods (Discriminant Function Analysis) and differences in 6 individual morphological traits using linear mixed models (ANCOVA). Additionally, divergence will be assessed according to the range from which individuals were collected (their putative native range) and according to their genetic composition (which subspecies they assigned 90% or more genetically in previous STRUCTURE analysis).

I am analyzing five morpohometric traits: total length, standard length, orbital length, head length, and body depth; and one meristic trait: the number of soft dorsal fin rays. 

To assess overall differentiation, I will use Discriminant Function Analysis on the five morphometric traits to determine the accuracy with which individual samples can be identified to their range or genetic identity. To assess individual differences, I will use linear mixed ANCOVA models that determine differences of each morphometric trait relative to total length. To assess the number of soft dorsal fin rays, I will use logistic regression on 13 or 14 fin rays to the proportion of the genetic composition assigned to a given subspecies.

### Data Info:

Here I provide summary information for my morphological analysis for easy access in the manuscript writing process. I give the number of samples with morphological data, and within those, the number of Northern SMB and Neosho SMB samples. I also give the number of individual samples that assigned 90 % or more to any one cluster and also had morphological data.

OMITTED AR24 BECAUSE IT ASSIGNS ALMOST 98 PERCENT TO SPOTTED BASS

### SAMPLE SIZES

#### Total samples with morphological data = 249
#### Total Northern Range = 65
#### Total Neosho Range = 184

#### Total samples with both morphological data and genetic data = 185
#### Total samples assigning 90 % or more to neosho or northern = 88
#### Total Pure Neosho = 17
#### Total Pure Northern = 71
#### Total Admixed = 97

### Total Length Data

#### Samples with Total Length data = 385
#### Neosho samples with Total Length data = 320
#### Northern samples with Total Length data = 65
#### Pure neosho Total Length samples = 55
#### Pure northern Total Length samples = 82

# Aim 5 - Map Building
### NSMB_Microsats_MAPS.Rmd

Purpose: I am building multiple-scale maps to show my sample distribution.

### Data Used:

#### Shape file data from the internet

# Unused Code

All code in this file is miscellaneous, unused code from the SMB Genetics and Morphology R Project