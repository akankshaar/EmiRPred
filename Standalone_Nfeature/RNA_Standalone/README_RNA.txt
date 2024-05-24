# Nfeature
# Introduction
Nfeature is developed for computing wide range of Nucleotide features from their nucleic acid sequences. More information on Nfeature is available from its web server https://webs.iiitd.edu.in/raghava/nfeature. This page provide information about standalone version of Nfeature. This standalone contains two scripts, their description is as follows:

#############################################################################################################################################################################################################################

-> Standalone for calculating Nucleotide features of RNA sequences:


**Important: To run this script 'Data' folder should be in the same directory.**

#Usage: Following is complete list of all options, you may get these options by "Nfeature_RNA.py -h"
usage: Nfeature_RNA.py [-h] -i INPUT [-o OUTPUT] -ft FEATURE [-k KVALUE] [-n NVALUE]
                [-c CVALUE] [-s SPLIT] [-or ORDER]
                [-p PROPERTY [PROPERTY ...]] [-l LAGVALUE] [-w WVALUE]
                [-lm LMVALUE] [-path PYTHONPATH]

optional arguments:
  -h, --help            show this help message and exit
  -i INPUT, --input INPUT
                        Input: protein or peptide sequence in FASTA format
  -o OUTPUT, --output OUTPUT
                        Output File name
  -ft FEATURE, --feature FEATURE
                        Select ALL_COMP, ALL_CORR and ALL_BIN to compute combined features of whole nucleotide sequence
                        ALL_COMP : all composition based features 
                        ALL_CORR : all correlation based features
                        ALL_BIN: all binary profile based features
                        Select among various features and include _NT,_CT,_REST,_SPLIT after feature name for N-Terminal,C-Terminal,Reamining of N-terminal and C-Terminal and for splitted sequence respectively.                        
                        CDK : kmer composition
                        RDK : Reverse Compliment kmer composition
                        DAC : Dinucleotide based auto correlation
                        DCC : Dinucleotide based cross correlation
                        DACC : Dinucleotide based auto cross correlation
                        PDNC :  Pseudo dinucleotide composition
                        PC_PDNC : parallel correlation pseudo dinucleotide composition
                        SC_PDNC : Serial correlation pseudo dinucleotide composition
                        NRI : Nucleotide repeat index
                        ES : Sequence level entropy of whole sequence
                        EN : Nucleotide level entropy of whole sequence
                        DDN : Distance Distribution of whole sequence
                        BPD : Binary profile dinucleotide
                        BPM : Binary profile Mono-Nucleotide
                        BP_DP : Dinucleotide properties
  -k KVALUE, --kvalue KVALUE
                        Enter the k value and by default it is set to 1
  -n NVALUE, --nvalue NVALUE
                        Enter the n value
  -c CVALUE, --cvalue CVALUE
                        Enter the c value
  -s SPLIT, --split SPLIT
                        Enter the split value
  -or ORDER, --order ORDER
                        Enter the order value and by default it is set to 1
  -p PROPERTY [PROPERTY ...], --property PROPERTY [PROPERTY ...]
                         Refer the property list of dipeptides and enter property names having space in between
  -l LAGVALUE, --lagvalue LAGVALUE
                        Enter the lag value and its default value is 2
  -w WVALUE, --wvalue WVALUE
                        Enter the w value and its default value is 0.05
  -lm LMVALUE, --lmvalue LMVALUE
                        Enter the lamada value and its default value is 1
  -path PYTHONPATH, --pythonpath PYTHONPATH
                        Enter the python environment path

#Parameters Description:

Input File: It allow users to provide input in the following format; 
		i) FASTA format (standard) (e.g. input.fa)

Output File: Program will save result in CSV format, in the provided filename.
		In case user do not provide output file name, it will be stored in output.csv.
		
Feature name: It allows users to choose the type of feature, the user want to calculate, such as CDK which stands for kmer composition.

k-Value: It allows user to compute features corresponding to particular mers. By default it is 1. Its value ranges from 1 to 3.

Property: It allows user to compute features according to the physicochemical property mentioned by the user.

Path: It allows user to provide python environment path.

N-terminal: It allows user to cut the specific number of nucleotides from the N-terminal of the sequences.
		
C-terminal: It allows user to cut the specific number of nucleotides from the C-terminal of the sequences.

REST-terminal: It allows user to cut the specific number of nucleotides from the N- and C-terminal of the sequences, and join them.

Split: It allow users to divided the sequence into number of sequences.

Order: It allows user to calculate higher order nucleotide features.

Lag : It defines the value for order of lag, to calculate certain features, by default it is set at 2.

Lambda : It defines the value for order of lambda, to calculate certain features, by default it is set at 1.

Weight: It defines the weight factor to calculate some features, by default it is set at 0.05.

Nfeature Package Files
=======================
It contantain following files, brief description of these files are given below:

LICENSE                  : License information

README.md                : This file provide information about this package

Nfeature_RNA.py         : Python program to calculate Nucleotide features based on RNA sequences

input_RNA.fa               : Example file contain nucleotide sequences in FASTA format

Requirement.txt          : This file consists of commands and pre-requisite to run the aforementioned scripts.
