# DNA Extraction 
## Starting DNA/RNA Quantification
    - For Hi-C library prep, starting material is cells or tissue
## Bioanalzyer results 
    - N/A
## Extraction kit, if facility extracted
    - N/A
# Library Preparation
1.  Library preparation kit
    - For project 1900, Phase Genomic Promixo Hi-C kit for animal samples (KT2045) was used for library preparation.

2. Library preparation
     - Five million cells (45ul) were used as per manufacturers recommendations.
    - A couple of issues occurred, which may or may not have required library reprep.  - The first library on Friday () and taken up to the reverse crosslinks steps for a 16 hour incubation.  Unfortunately, I was unable to come in the following day to take out the reaction tubes.  By Sunday, the reaction had evaporated down to about 10ul from 105ul.  I thought the reaction was cooked, so decided to set up another library.  The second library was performed up to the DNA purification step, when I discovered I was using the wrong manual.  The newerprotocol uses 2.5X the amount of 100% Ethanol to add to the Recovery Wash Buffer.  With not enough ethanol in the wash buffer, I though surely, I washed the DNA off the beads.  I contacted PacBio tech support and they thought it should be okay.  I decided to go ahead and add the appropriate amount of ethanol to the Recovery wash buffer and proceed with both libraries.
    - I brought the evaporated reaction up to the correct concentration with nuclease free water
    - Qubit reading for samples following binding the sample to the streptavidin beads.
        1.  0.0748 ng/ul (15ug total mass)
        2.  0.0672 ng/ul (13ug total mass)
    - Based off these amounts, the adapter was not diluted.
    - The protocol was completed without incident.
        
3.  Indexes
    - Indexes C3 and H3 were used for library 1 and library 2, respectively. 

4.  Library QC
    - Final concentration of the libraries (measured using Qubit DNA HS)
        1. 60 ng/ul
        2. 45 ng/ul
    - Concentrations were good.  The PacBio support person indicated that both librariew wer probalby good.
    - Size of the libraries measured on a Bioanalzyer using DNA HS kit were 443 for library 1 and 394 for library 2.
    - It was decided to sequencing library 1.

5.  Pooling, pool QC and Sequencing
    -Since only one library was being sequenced, pooling was not necessary.  The library was diluted to 4nM by diluting it 1:51 in EB buffer.  High sensitivity Qubit quantification on the dilution gave a concentration of 1.48ug/ul or ~5nM.  To get the library to it's final concentration of 1.5nM, the library was diluted agin 6/20 in EB buffer (x vol * 5nM) = (20ul * 1.5nM). The final library concentration based on high senditivity DNA Qubit was 0.462ng/ul (1.6nM)
    -The library was sequenced on lane 2 of a 2X150 NovaSeq SP flowcell using the XP loading protocol and another customer's sample in lane 1

# Analysis
## Data was analyzed on the Facilities server with bcl2fastq using the command :
      
            time nohup /mnt/GIF-NAS_Illumina_Data/bcl2fastq/bin/bcl2fastq --runfolder-dir /mnt/GIF-NAS_Illumina_Data/230317_A01171_0153_AH2T2JDRX3/ --output-dir /mnt/GIF-NAS_Illumina_Data/230317_A01171_0153_AH2T2JDRX3/Unaligned --sample-sheet /mnt/GIF-NAS_Illumina_Data/230317_A01171_0153_AH2T2JDRX3/2275_nextgen_2023-02-27.csv --use-bases-mask y*n,n*,n*,y*n
            



