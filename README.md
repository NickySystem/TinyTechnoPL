# Tiny Techno Pseudo Language  
Open main.pd in Pure Data (www.puredata.info)  
In a terminal, navigate to your pd directory.  

Into the /bin folder  

run the following: **pdsend 6000 localhost udp**  

Then you can control the audio engine with the following commands...  

## Global  
start *1/0*  
bpm *num*  

## Kick Drum  
Kick play *num*  
kick mod *num*  
kick on *1/0*  
kick hp *num*  
Kick vol *num*  
Kick sample *filepath*  

## Snare Drum  
Kick play *num* (step to play kick)  
kick mod *num* (number of steps in a sequence)  
kick lp *num* (low pass filter in Hz)  
Kick vol *num* (amplitude - 1 is at level of sample)  
Kick sample *filepath*  

## Closed Hat  
hhc all  
hhc none  
hhc vol *num*  
hhc del *0 - 5000*  
hhc binary *0 0 1 0 0 0 1 0*  
hhc offset *0-8*  

## Open Hat  
hho play *num*  
hco mod *num*  
hho hp *num*  
hho vol *num*  
hho sample *filepath*  

## Euclidean Clap  
clap mod *0-16*  
clap steps *0 to above mod*  
clap offset *0 to above mod*  
clap bit *0-16*  
