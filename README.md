Affine Gap Penalty Alignment
========================
Griffen Mustion (gmustion35@gmail.com) -- Final Project for CS 466 - Intro to Bioinformatics at UIUC

BLOSUM62 & the Triangle Inequality
------------------------
First we'll show that the BLOSUM62 scoring matrix does not satisfy the Triangle Inequality for all valid triples.

Global Alignment
------------------------
Here we will do the bulk of the work creating a global alignment algorithm which will admit affine gap penalties. This is accomplished by modifying the standard global alignment recurrence to consider additional matrices representing opening, extending, and closing indel gaps. In this manner, we convert our two-dimensional dynamic program to three-dimensions. We must also modify the standard traceback algorithm so that it can follow our alignment back through the opening and closing of gaps.

Fitting and Local Alignments
------------------------
Converting our global alignment algorithm to work for fitting and local alignments only requires simple modifications to the conditions of our recurrence and the beginning/termination conditions of our traceback.

Dataset
------------------------
Our alignment algorithms will be tested with protein sequences belonging to the Peptidase C14 domain of the caspase family. All sequences have been sourced from the InterPro (Pfam) Database. https://www.ebi.ac.uk/interpro/entry/InterPro/IPR011600/
