# **CAFE**
**aCcelerated Alignment-FrEe sequence analysis**

===================

Thank you for downloading CAFE for molecular sequence analysis using state-of-art Alignment-Free methods. This software provides the well-optimized programs to compute overall **28** distance/dissimilarity measures including (1) conventional measures based on k-mer counts, (2) newly developed measures based on background adjusted k-mer counts, and (3) measures based on presence/absence of k-mers. The detailed definitions can be found in the paper. 

CAFE works with sequence data, both long genomic sequences and shotgun sequence reads from NGS technologies, and subsequently generates pairwise dissimilarities among the sequences as output. CAFE provides four types of visualized downstream analysis, including heatmap, two dimensional projection using principal coordinate analysis (PCoA), network display, and sequence clustering into a dendrogram by using the neighbour-joining algorithm. All the analysis can be performed by simply clicking through well-designed graphical user interface (GUI) on two common operating systems ( Mac and Windows) or invoking a stand-alone command line executable program on three common operating systems (Linux, Mac, and Windows)


One-click Installation
============
<font color="red">(DO NOT download using the “clone or download” button above)</font>

Installation on Windows
------------------------
> 1. Download the Windows Version of CAFE  from [**here**](https://www.dropbox.com/s/o2d6z5pze8ih7iw/CAFE_v071017.zip?dl=0) or [**here**](http://pan.baidu.com/s/1gfJ1mQB)
> 2. Unzip it
> 3. Due to permission settings of User Account Control in different version of windows, the default executable of **cafe_win.exe** may not work as expected. To test it, just double-click **cafe_win.exe** or run it through the command line. If there is some alert or errors, please rename **cafe_win_2.exe** or **cafe_win_3.exe** to **cafe_win.exe** and repeat until passing the test. 
> 4. Within the folder, double-click **CAFEGUI.exe**. Be patient for the first time. If it fails again, try to right-click **CAFEGUI.exe** and 'Run as administrator'.

Installation on Mac
------------------------
> 1. Download the Mac Version of CAFE  from [**here**](https://www.dropbox.com/s/i3rsu8steiwemzd/CAFE_mac_latest.zip?dl=0) or [**here**](http://pan.baidu.com/s/1kUIwHbL)
> 2. Unzip it
> 3. Within the folder, double-click **CAFEGUI**. If fails, please use the terminal to execute "./CAFEGUI".


Usage
=====

Guidance on Graphical User Interface
------------------------

<p align="center">
  <img src="https://raw.githubusercontent.com/younglululu/CAFE/master/image/snapshot1.jpg"/>
</p>
The graphical user interface has the layout shown in the above figure, containing six parts in terms of functionality:

The red area corresponds to the Data Selection Toolbar. The sequence data can be either long genomic sequences or shotgun sequence reads from NGS technologies, with the file extension '.fasta', '.fa' or '.fna'. 

![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/load.gif) : Load Existing Results in Phylip format.

![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/addFile.gif)  :  Add one genome sequence to the list.

![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/addDir.gif)  :  Add all genome sequences from directory to the list.

![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/remove.gif)  :  Remove Selected genome sequences in the list.

![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/clear.gif)  :  Remove all genome sequences in the list.

The yellow area involves parameter configuration related to various distance measures, including the selection of 28 distance measures, k-mer length, potential Markov Order encoding the sequence model, the threshold cutoff of the k-mer occurrences, and whether to consider the reverse complement of each k-mer, which  is a common practice in dealing with shotgun sequence reads from NGS technologies. Usually the potential Markov Order remains unclear to the user. The simple yet time-consuming way is to choose '-1' as inferring the optimal Markov Order automatically by using the Bayesian Information Criterion (BIC).

The pink area corresponds to the Image Toolbar. When the visualized results have been plotted, users can either zoom in or zoom out the figure by clicking the button or using the mouse wheel. Meanwhile, the figure can be saved locally by  clicking the button or right-clicking the mouse.

![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/zoomin.gif) : Zoom in the current figure.

![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/zoomout.gif) : Zoom out the current figure.

![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/save.gif) : Save the current figure.

The green area contains the list of all sequence added from the Data Selection Toolbar.

The blue area keeps track of the running information when calculating the distance measures. 

The purple area contains the key to visualize the relationship among the input sequences using different approaches. Specifically,  CAFE provides four types of visualized downstream analysis, including heatmap, two dimensional projection using principal coordinate analysis (PCoA), network display, and sequence clustering into a dendrogram by using the neighbour-joining algorithm. Each analysis is shown in the respective tabbed window.


An Usage Example of Graphical User Interface
------------------------


Here we go through a toy example step-by-step.  You can find a folder named "example" in the unzipped folder.

We first click the ![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/addDir.gif) button of the Data Selection Toolbar and select the "data" folder, selecting all the virus genome sequence files into the input list.

<p align="center">
  <img src="https://raw.githubusercontent.com/younglululu/CAFE/master/image/snapshot2.jpg"/>
</p>


We then specify the alignment-free distance. Here we choose Manhattan distance measure, and simply click the 'Run' button, with default k-mer length setting ( K=8 ). Then calculated pairwise distances will be saved into a file named 'result.Ma.phylip'. The file is saved in standard phylip format. Meanwhile, the result is available in visualized plots. Also, we can track the progress through the console in the left panel.

<p align="center">
  <img src="https://raw.githubusercontent.com/younglululu/CAFE/master/image/snapshot4.jpg"/>
</p>

Notice that users can always load previously saved phylip results for visualization by clicking the ![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/load.gif) button of the Data Selection Toolbar! 

<p align="center">
  <img src="https://raw.githubusercontent.com/younglululu/CAFE/master/image/snapshot5.jpg"/>
</p>

Once the visualized results have been plotted, users can either zoom in or zoom out the figure by clicking the ![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/zoomin.gif) and ![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/zoomout.gif) buttons or using the mouse wheel. Meanwhile, the figure can be saved locally by clicking the ![alt tag](https://raw.githubusercontent.com/younglululu/CAFE/master/code/image/save.gif) button or through the popup menu by right-clicking the mouse.

Here is the dendrogram of the pairwise distances by using the neighbour-joining algorithm. 

<p align="center">
  <img src="https://raw.githubusercontent.com/younglululu/CAFE/master/image/snapshot6.jpg"/>
</p>

Here is the two dimensional projection using principal coordinate analysis (PCoA).

<p align="center">
  <img src="https://raw.githubusercontent.com/younglululu/CAFE/master/image/snapshot7.jpg"/>
</p>

Here is the heatmap.

<p align="center">
  <img src="https://raw.githubusercontent.com/younglululu/CAFE/master/image/snapshot8.jpg"/>
</p>

Here is the network analysis with respect to the 10% quantile of the edges with smallest distance as weight.

<p align="center">
  <img src="https://raw.githubusercontent.com/younglululu/CAFE/master/image/snapshot9.jpg"/>
</p>



Usage of  Stand-alone Executable Program
------------------------

> **Command:  ** ./cafe [options]* -D  < dist > -I < fa_files > -K  < intK >

> - Main arguments:

	-D < dist >: Comma-separated list of distance measurements,  **E.g.** -D D2star,Ma,CVtree. The options include: 
	
		Conventional measures based on kmer counts :		
			 
				1. Ch: Chebyshev distance
				
				2. Canberra: Canberra distance
				
				3. Chisq: Chi-Square distance
				
				4. Cosine: Cosine distance
				
				5. Co-phylog: Co-phylog distance
				
				6. D2: D2 distance
				
				7. Eu: Euclidean distance
				
				8. FFP: Feature frequency profiles (FFP)
				
				9. JS: Jensen-Shannon divergence
				
				10. Ma: Manhattan distance
				
				11. Pearson: Pearson distance
				
		Newly developed measures based on background adjusted kmer counts: 
			 
				1. CVtree: CVtree distance
				
				2. D2shepp: D2shepp distance
				
				3. D2star: D2star distance
				
		Measures based on presence/absence of kmers:

				1. Anderberg: Anderberg distance
				
				2. Antidice: anti-Dice distance
				
				3. Dice: Dice distance
				
				4. Gower: Gower distance
				
				5. Hamman: Hamman distance
				
				6. Hamming: Hamming distance
				
				7. Jaccard: Jaccard distance
				
				8. Kulczynski: Kulczynski distance
				
				9. Matching: Matching distance
				
				10. Ochiai: Ochiai distance
				
				11. Phi: Pearson Phi distance
				
				12. Russel: Russel-Rao distance
				
				13. Sneath: Sneath-Sokal distance
				
				14. Tanimoto: Rogers-Tanimoto distance
				
				15. Yule: Yule distance
				
	-F < fa_Dir >: Folder containing only fasta files with extension '.fasta', '.fa', and '.fna'.
	
	-I < fa_files >: Comma-separated list of sequence fasta files, e.g. -I speciesA.fa,speciesB.fa,speciesC.fa. Pairwise similarity is calculated based upon the sequences specified with this option.
	
	-K < intK >: Kmer Length.

> - Options:

	-J < jfexe_path >: Use jellyfish to accelerate kmer counting. <jfexe_path> denotes the file path of jellyfish executable file, e.g. jellyfish-2.2.4/bin/./jellyfish
	
	-L < lower >: Only consider k-mer with occurrence >= <lower>. The default value is 0.
	
	-M < order >: Markov Order involved in D2star, D2shepp and JS. There are two possible options. The first option is one single value indicating that all the sequences use the same order. The second option is comma-separated list of orders. Notice that the length of the list should match the number of fasta files. The order value could be non-negative integer but less than Kmer length or \"-1\" with the special intention to automatically infer the suitable order (not suitable for JS). The default Markov Order is -1 as inferring the optimal Markov Order automatically by using the Bayesian Information Criterion (BIC).
	
	-R: Consider Reverse Complement in kmer counting.
	
	-S < dir >: Save/Load calculated k-mer count binary files to the folder < dir >. Each input fasta file corresponds to particular model.
	
	-O < path >: Output results to file at < path >.
	
	-T < type >: The output type as the input to downstream analysis, including: plain, [phylip](http://evolution.genetics.washington.edu/phylip.html) (as hierarchical clustering), [cytoscape](www.cytoscape.org/) (as network analysis) and mds (Multidimensional Scaling as 2D plotting). E.g. -T mds. The default type is plain.

> - Examples:

	./cafe -M 0 -O output_path -S model_dir -T plain -I speciesA.fa,speciesB.fa -J /panfs/cmb-panasas2/ylu465/jellyfish-2.2.4/bin/./jellyfish -K 10 -D D2star,Ma
	
	./cafe -M 0 -S model_dir -I speciesA.fa,speciesB.fa -J /panfs/cmb-panasas2/ylu465/jellyfish-2.2.4/bin/./jellyfish -K 10 -D D2star,Ma
	
	./cafe -M 0 -L 2 -I speciesA.fa,speciesB.fa -J /panfs/cmb-panasas2/ylu465/jellyfish-2.2.4/bin/./jellyfish -K 10 -D D2star,Ma -R



Contacts and bug reports
========================

Please send bug reports, comments, or questions to 

Yang Lu: [ylu465@usc.edu](mailto:ylu465@usc.edu)

Prof. Fengzhu Sun: [fsun@usc.edu](mailto:fsun@usc.edu)


----------

Copyright and License Information
=================================


This software is Copyright © 2018 The University of Southern California. All Rights Reserved.

This program is under the terms of USC-RL v1.0 License. 

Permission to use, copy, modify, and distribute this software and its documentation for educational, research and non-profit purposes, without fee, and without a written agreement is hereby granted, provided that the above copyright notice, this paragraph and the following three paragraphs appear in all copies. 

Permission to make commercial use of this software may be obtained by contacting:
USC Stevens Center for Innovation
University of Southern California
1150 S. Olive Street, Suite 2300
Los Angeles, CA 90115, USA

This software program and documentation are copyrighted by The University of Southern California. The software program and documentation are supplied "as is", without any accompanying services from USC. USC does not warrant that the operation of the program will be uninterrupted or error-free. The end-user understands that the program was developed for research purposes and is advised not to rely exclusively on the program for any reason.

Last update: 08-May-2018
