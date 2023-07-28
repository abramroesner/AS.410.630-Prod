# AS.410.630-Prod
A Python program called orfs to find all the open reading frames (ORFs) in the 
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
- Print your output in FASTA format, with one header line for each ORF, followed by the 
DNA in the ORF. 
- The header should be the same as the header in the input file, 
followed by a bar "|" followed by  
- FRAME = indicates the frame number (1-6) 
- POS = is the genomic position of the start of the ORF (left end is base 1) 
- LEN = is the length of the ORF (in bases)  
 
If N = 4, 5 or 6, then POS should be a negative number that indicates the 
position of the start of the ORF from the right end of the sequence.  
 
The DNA in the ORF should be printed out with a space between each codon, and no 
more than 15 codons per line.  
For example:  
> AE000111.1| Escherichia coli K-12 | FRAME = 1 POS = 5215 LEN = 138  
ATG ATA AAA GGA GTA ACC TGT GAA AAA GAT GCA ATC TAT CGT ACT 
CGC ACT TTC CCT GGT TCT GGT CGC TCC CAT GGC AGC ACA GGC TGC 
GGA AAT TAC GTT AGT CCC GTC AGT AAA ATT ACA GAT AGG CGA TCG TGA 
