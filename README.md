# VDPtools

## 1. Introduction
Variety discrimination power (VDP) is an Appraisal Index for Loci Combinations Screening Applied in Plant Variety Discrimination.VDP refers to the overall capability of a certain loci combination to distinguish all given varieties calculated by certain statistic method, based on the fact that the genotype of a loci combination can be used to identify a certain variety of plant. 

VDP contains three statistic methods, i.e. probability-based variety discrimination power (P-VDP), comparison-based variety discrimination power (C-VDP), ratio-based variety discrimination power (R-VDP). Total probability of discrimination Power (TDP) is a comprehensive capability appraisal index used to identify individual by multiple loci. In order to compare the calculation results of the three methods and TDP, we developed the software called "VDPtools", which can calculate the values of TDP, P-VDP, C-VDP and R-VDP.

## 2. System Requirement & Installation
VDP is developed based on the C # programming language of the Visual Studio development environment. It can only run on Windows XP or later operating systems. You need to ensure that the computer has `.Net Framwork 4.0` and above.

The program does not require any installation steps, Just click the file to run.
```diff
! VDPtools.exe
``` 

## 3. Data Preparation
The software needs to input two csv files: one is a data file, which contains the genotype data of the sample to be evaluated; the other is a locus file, which contains the locus number of the locus combination to be evaluated. 

The types of molecular markers supported by the data file include simple sequence repeats (SSR) and single nucleotide polymorphism (SNP). The data structure supported by the data file includes two types: loci in rows and samples in columns, or samples in rows and loci in columns. For the specific format, please refer to the two demo files "SSR data (row-samples col-loci) .csv" and "SNP data (row-loci col-sample) .csv" provided by this project.

In the locus file, loci combinations are in rows, and loci are in columns. The first column represents the sequence number of the locus combination, and the second column represents the specific locus contained in the locus combination. It is represented by the serial number of the locus in the data file. The sequence number of the locus starts from 0, and 0 represents the first locus.

## 4. Method of Operation
Please follow the steps prompted by the main interface.

*Step1: Set the molecular marker type of the data file.<br>
*Step2: Set the data structure of the data file.<br>
*Step3: Enter the path of the data file and the loci file. When this step is completed, changes are not allowed in steps 1 and 2. To make changes, please restart the program or click the open button of the data file and click Cancel to reset the input of the above steps.<br>
*Step4: Choose one of the variety threshold setting methods and enter the corresponding threshold.<br>
*Step5: Select an appraisal index for loci combination screening.<br>
*Step6: Set the number of base pairs of different alleles, when the molecular marker type of the data file is SSR.<br>
*Final: Click `"OK"` button to run the program. When statusStrip shows 
```diff
- Run done! Time:0h0m0s8ms
```
click `"Open Result Folder"` button to find the `.csv` output file e.g. 
```diff
+ R-VDP_DataFileName_FinishDate_FinishTime.csv, C-VDP_DataFileName_FinishDate_FinishTime.csv ....
``` 

## 5. Interpretation of Result
The data structure of the output file corresponds to that of the loci file. Each row of the output file represents the calculation result of a loci combination. The first column represents the number of the site combination, which is consistent with the first column of the loci file. The second column is the calculation result corresponding to the appraisal index selected in step 5 of the program. When the appraisal index selected in step 5 of the program is R-VDP, the sample_id that cannot be recognized by the loci combination will be displayed from the third column. Other methods will not display the unrecognized sample_id results.

## 6. Citation
Please see and cite our paper: Yang,Y. et al. Variety discrimination power: An Appraisal Index for Loci Combination Screening Applied to Plant Variety Discrimination  (In preparation)

## 7. Contact Us
Please send your comments and suggestions to caurwx@gmail.com.
