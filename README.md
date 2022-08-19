# Tiny Techno Pseudo Language  
Open main.pd in Pure Data (www.puredata.info)  
In a terminal, navigate to your pd directory.  

Into the /bin folder  

run the following: **pdsend 6000 localhost udp**  

Then you can control the audio engine with the following commands...  

## Global  
start *1/0* (start or stop metronome)  
bpm *num* (change bpm)  

## Kick Drum  
Kick play *num* (step of sequence to play)  
kick mod *num* (length of sequence)  
kick hp *num* (high pass filter in Hz)  
Kick vol *num* (volume 0 -1)  
Kick sample *filepath* (not yet implemented)  

## Snare Drum  
Kick play *num* (step of sequence to play)  
kick mod *num* (length of sequence)  
kick lp *num* (low pass filter in Hz)  
Kick vol *num* (volume 0 -1)  
Kick sample *filepath* (not yet implemented)  

## Closed Hat  
hhc all (play all 16ths)  
hhc none (play nothing)  
hhc vol *num* (volume 0 -1)  
hhc del *0 - 5000* (delay by Ms)  
hhc binary *0 0 1 0 0 0 1 0* (binary pattern 8 steps)  
hhc offset *0-8* (offset pattern)  

## Open Hat  
hho play *num* (step of sequence to play)  
hco mod *num* (length of sequence)  
hho hp *num* (high pass filter in Hz)  
hho vol *num* (volume 0-1)  
hho sample *filepath* (not yet implemented)  

## Euclidean Clap  
clap mod *0-16* (length of sequence)  
clap steps *0 to above mod* (number of steps to fill)  
clap offset *0 to above mod* (offset pattern)  
clap bit *0-16* (bit crush 1-16bits)  
clap vol (volum 0-1)
