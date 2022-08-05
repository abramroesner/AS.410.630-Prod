# AS.410.630-Prod
Group project for JHU course
Final Group Project   
What is expected:  
You will be divided into teams of 3 or 4. The assignment is simple as described below, 
but what I will be most looking at is how you work together and how you divide the tasks 
among yourselves. At the end of the semester I will ask each of you to evaluate your 
other team mates performance. You will be asked to email me directly and give each of 
them a score (from 1 to 10) representing how much they contributed.  Keep in mind that 
everyone has to code! Meaning someone can’t just write the report and say that was  
his\her contribution! You need to meet with your group and decide how to divide up the 
program into functions and then who will do which one. All of this interaction should 
occur in Black Board (the group’s discussion board). If you chat outside of Black Board 
then please post a transcript of your chat in there for me to see (and a record for 
yourselves as well).  
Deliverable:  
Each group will submit a 1-2 page report (not including the code), summarizing the work 
they did to solve the problem (including how the problem was divided up among the 
group members), what obstacles they had, and any future improvements that need to 
be made. The code should be fully documented and well commented. For every 
function the name of the primary author(s) should be included (as comments).  
Project Description:  
Given the genomic sequences for an organism; one of the first steps in identifying the 
genes is to identify the open reading frames (ORFs). An open reading frame is a 
maximal length sequence of the DNA that starts with a start codon ATG and ends with a  
stop codon (TAA, TAG or TGA). In prokaryotes, genes may occur within ORFs. In 
eukaryotes, the story is complicated by the presence of introns that are spliced out of 
the mRNA before translation. In this assignment, you will write a Python program that 
finds all the ORFs in a genomic sequence.   
A genomic sequence has 6 reading frames, corresponding to the six possible ways of 
translating the sequence into three-letter codons. Frame 1 treats each group of three 
bases as a codon, starting from the first base. Frame 2 starts at the second base, and 
frame 3 starts at the third base. Frames 4, 5 and 6 are defined in a similar way, but refer 
to the opposite strand, which is the reverse complement of the first strand.  
Specifications:   
Write a Python program called orfs to find all the open reading frames (ORFs) in the 
input sequence.  
INPUT:  
The program will take in as input a file, which will contain any number of DNA 
sequences in the FASTA format:  
- A line beginning with a ">" is the header line for the next sequence - All lines after the 
header contain sequence data.  
- There will be any number of sequences per file.  
- Sequences may be split over many lines.  
- Sequence data may be upper or lower case.  
- Sequence data may contain white space, which should be ignored.  
Ask the user for the minimum ORF to search for. The default is 50, which means your 
program should print out all ORFs with at least 50 bases.  
OUTPUT:   
Print your output in FASTA format, with one header line for each ORF, followed by the 
DNA in the ORF. The header should be the same as the header in the input file, 
followed by a bar "|" followed by  
FRAME = indicates the frame number (1-6) 
POS = is the genomic position of the start of the ORF (left end is base 1) 
LEN = is the length of the ORF (in bases)  
 
If N = 4, 5 or 6, then POS should be a negative number that indicates the 
position of the start of the ORF from the right end of the sequence.  
 
The DNA in the ORF should be printed out with a space between each codon, and no 
more than 15 codons per line.  
For example:  
> AE000111.1| Escherichia coli K-12 | FRAME = 1 POS = 5215 LEN = 138  
ATG ATA AAA GGA GTA ACC TGT GAA AAA GAT GCA ATC TAT CGT ACT 
CGC ACT TTC CCT GGT TCT GGT CGC TCC CAT GGC AGC ACA GGC TGC 
GGA AAT TAC GTT AGT CCC GTC AGT AAA ATT ACA GAT AGG CGA TCG TGA 
