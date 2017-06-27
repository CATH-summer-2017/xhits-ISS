##xhits-ISS

#### 1. Define your questions and aims.
* This project concerns using ISS to facilitate the superfamily (SF) merging decisions.
* SF consists of structural representatives (s-reps). However, s-rep from one SF (SF1) might appear homologous to a s-rep from another SF (SF2). This identified homology is called a "crosshit"(xhit) because this "hit" is across superfamilies.
* Detection of crosshits suggests revision of the boundary of superfamilies. If the two SF's show many xhits inbetween, then one may consider merging the two SF's into one.
* The emergence of Xhit partially results from discovery of new structure/sequence intermediates. These intermediates mark out an evolutionary pathway between the two SF's, and allow one to conclude a relationship.  
* One is advised that this xhit problem has its origin in definition of SF's and protein domains. 
#### 2. Build up your test suites.
* The objective of ISS is to provide information on whether the two SF should be merged. Previously, this is done by PRC, HMM, and SSAP (detailed implementation yet to assess). 
* The idea of ISS is to derive evolutionary distance between s-reps using their profiles. Each s-rep is projected onto a hit list in sequence space, using HMMscan. (In other words, the whole sequence database is scanned with the profile). The two hit lists are then compared in some ways to suggest whether the profiles are related.
* To test for its functionality, we could simulate the situation of some earlier merges, and check whether ISS successfully propose the human decision. See [crosshit_notes](http://trac.cathdb.info/projects/cath/wiki/CrossHitsV410Notes#no1).

#### 3. Things to be constructed.
* Pull profiles and s-reps from CATH.
* HMMscan module to process a s-rep/profile into a hit-list
* ISS algo to compare two hit-lists.