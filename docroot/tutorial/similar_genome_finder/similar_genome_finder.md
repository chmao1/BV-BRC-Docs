# Similar Genome Finder Service

*Revised: 1/25/2022*

When a researcher has a new genome sequence, one of the first things they want to identify is the closest relatives of their genome. BV-BRC provides a new service that allows researchers to do this using Mash/MinHash[1]. Mash reduces large sequences and sequence-sets to small, representative sketches, from which global mutation distances can be rapidly estimated. The MinHash dimensionality-reduction technique to include a pairwise mutation distance and P value significance test, enabling the efficient clustering and search of massive sequence collections.

1.	At the top of any BV-BRC page, find the Services tab. Click on Similar Genome Finder. 
![Figure 1](./images/Picture1.png "Figure 1") 

2.	This will open up the Similar Genome Finder landing page.
![Figure 2](./images/Picture2.png "Figure 2") 

## Loading a BV-BRC genome 

1\.	To load a genome that has been privately annotated BV-BRC, click on the filter icon that is at the left side of the text box under **Search By Genome Name Or Genome ID**.
![Figure 3](./images/Picture3.png "Figure 3") 

2\.	This will open a box that allows a researcher to search across all of the public genomes available in BV-BRC, or across the genomes that they have annotated and that are stored in their private workspace. To select private genomes, deselect the Public Genomes box. This will leave the Private Genomes box selected. The filter can be used to narrow the search for each of the categories.

![Figure 4](./images/Picture4.png "Figure 4") 

3\.	Click the down arrow at the right of the text box under **Search By Genome Name Or Genome ID**. This will open a drop-down box that shows all of the researcher’s private genomes, which have a lock icon in front of them.  To select a specific genome, scroll down and find the genome of interest, and then click on it.
![Figure 5](./images/Picture5.png "Figure 5")

4\.	This will autofill the name of the genome in the text box. To see options that can be adjusted, click on the down arrow to the right of Advanced Options.
![Figure 6](./images/Picture6.png "Figure 6") 

5\.	Alternatively, it is not necessary to use the filters for different types of public genomes, or the private genomes.  Entering the name, or the genome ID in the text box will open a drop-down box that shows possible matches.  Note that reference genomes are denoted with a **[Ref]** in front of the name.  Representative genomes would have a **[Rep]** and private genomes have the lockbox icon seen above.  All of the other public genomes have no indicator in front of the name.  Clicking on the genome of interest will autofill the box as seen above.
![Figure 7](./images/Picture7.png "Figure 7") 

## Loading a genome that is not in BV-BRC

1\.	The Similar Genome Finder tool is one of the few places in BV-BRC, outside of the Assembly and Annotation pipelines, where genomes that have not been annotated in BV-BRC can be explored. To do this, click on the folder icon that is at the end of the text box underneath **Or Upload FASTA/FASTQ**. 
![Figure 8](./images/Picture8.png "Figure 8") 

2\.	This will open a pop-up window that has a direct link to the workspace.  To upload a new file, click on the **Upload** icon at the top right of that window.
![Figure 9](./images/Picture9.png "Figure 9") 

3\.	This will open a new pop-up window.  Note that it is pre-selected for **Contigs**, but if reads are desired, the type will need to be changed.  To interface with your computer, click on the Select File button.
![Figure 10](./images/Picture10.png "Figure 10") 

4\.	An interface with your computer will open.  Note that fasta files will be highlighted if Contigs were selected.   If read files were selected, fastq files would be highlighted.  Click on the desired file, and then click on the **Open** button at the lower right of the window.
![Figure 11](./images/Picture11.png "Figure 11") 

5\.	This will go back to the pop-up window where the name of the selected file is listed below the words **File Selected**.  Click on the **Start Upload** button at the lower right.
![Figure 12](./images/Picture12.png "Figure 12") 

6\.	The progress of the upload can be seen on the upload monitor at the lower right of the page.  Contig files generally load quickly.  Read files, which are often quite large, can take more time.
![Figure 13](./images/Picture13.png "Figure 13") 

7\.	Once the upload is complete the name of the file will appear below the words **Or Upload FASTA/FASTQ**.
![Figure 14](./images/Picture14.png "Figure 14") 

## Parameters

1\.	Researchers can adjust the number of hits that they want to see.  You can select 1, 10, 50, 100 or 500 hits to be returned by clicking on the down arrow next to the Max Hits box.
![Figure 15](./images/Picture15.png "Figure 15")

2\.	Since MinHash distances are probabilistic estimates, it is important to consider the probability of seeing a given distance by chance.  Mash provides p-values with distance estimations. Lower p-values correspond to more confident distance estimations and will often be rounded down to 0 due to floating point limits. If p-values are high (above, say, 0.01), the 𝑘-mer size is probably too small for the size of the genomes being compared.  You can select the P-Value threshold by clicking on the down arrow that follows the text box.
![Figure 16](./images/Picture16.png "Figure 16") 

Mash reduces large sequences and sequence-sets to small, representative sketches, from which global mutation distances can be rapidly estimated. The Mash distance approximates the mutation rate.  You can select the distance by clicking on the down arrow that follows the text box under **Distance**. Smaller numbers indicate a closer relationship. Additional information on how distance is calculated for Mash is available here: https://mash.readthedocs.io/en/latest/distances.html.
![Figure 17](./images/Picture17.png "Figure 17") 

4\.	Searches against the NCBI reference and representative genome dataset (https://www.ncbi.nlm.nih.gov/refseq/about/prokaryotes/) or all of the public genomes available in BV-BRC.  Selection of the database is available under **Scope**.
![Figure 18](./images/Picture18.png "Figure 18") 

## Submitting the job

1\.	Once the parameters of interest have been selected, click the **Search** button at the bottom of the page.
![Figure 19](./images/Picture19.png "Figure 19") 

## Job Results

1\.	The tool will return the top hits to the selected genome.  The page will include a reference to the data that was submitted for analysis, as well as the table.  The entire table can be downloaded by clicking on the **Download** icon at the top upper right of the table.
![Figure 20](./images/Picture20.png "Figure 20") 

2\.	The table also includes the metadata for the genomes, which includes the country of isolation, any host that the genome was isolated from, the year the strain was collected, and the data that it was completed.  Also included are the distance and P values, and the number of K-mers, out of 1000 total, that the genome shared with the submitted genome.
![Figure 21](./images/Picture21.png "Figure 21") 

3\.	To see information on an individual genome, click on the check box preceding it in the first column.  This will populate the box to the right of the vertical green bar with the information that BV-BRC has on that particular genome.
![Figure 22](./images/Picture22.png "Figure 22") 

4\.	The genomes can also be grouped together, and this group can be used in other BV-BRC tools like the Phylogenetic Tree service, the Protein Family Sorter, or the Proteome Comparison service.  Click on the check boxes for the desired genomes, and then click on the **Group** icon in the vertical green bar.
![Figure 23](./images/Picture23.png "Figure 23") 

5\.	This will open a pop-up box.  To create a new group, click on the down arrow at the end of the text box that has the words Existing Group.  Click on New Group, and then name it in the text box under Group Name.  Once this has been completed, click on the **Add** button at the bottom right of the box. This will successfully create a new group, which will be available in the workspace, and also when a tool using genome groups is launched.
![Figure 24](./images/Picture24.png "Figure 24") 

## Submit a new job

1\.	A new job can be submitted by clicking on the Edit form and resubmit button above the table.  This will reload the page, showing the previously submitted data. New data can be uploaded, and the parameters can also be adjusted.  
![Figure 25](./images/Picture25.png "Figure 25") 

## References

1.	Ondov, B.D., et al., Mash: fast genome and metagenome distance estimation using MinHash. Genome biology, 2016. 17(1): p. 1-14.

