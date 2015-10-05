# Vuoto

Example of shower analysis

To make the pythia customized output, modify the configuration file (main12.cc).
118 - 119 make the txt file with a list of momenta (and pid if you want to),
l55 you set the precision, making the file ligther.

l48 you turn hadronization off (easier to analyse, not big impact in physics).
    - if you turn off also parton level you will have the same file in parton level (decaying the higgses only)
    - usually I use the ".decayed" and ".shower" to indicate what is there, a ".decayed" example is uploaded there

l50 you say to not decay b-quarks - this will be our "btag"

Repository with one analysis code to this file linked to fastjet and root is [1]. 
 - output histograms, you can adapt to whatever we want

The file to run is the Vuoto.cc , instructions to run in the reader.
It calls Functions.cc and return the number of jets and leptons

In Functions.cc, in special, there is "recojets" function that applies Mass Drop + Filtering by the moment.
Prunned mass is out of box (see fastjet manual) n-subjetiness needs FastJetContrib and adaptation in Makefile.

