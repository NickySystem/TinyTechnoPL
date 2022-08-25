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
kick play *num* (step of sequence to play)  
kick mod *num* (length of sequence)  
kick hp *num* (high pass filter in Hz)  
kick vol *num* (volume 0 -1)  
kick sample *filepath* (load a sample, omit the .wav extension)  

## Snare Drum  
snare play *num* (step of sequence to play)  
snare mod *num* (length of sequence)  
snare lp *num* (low pass filter in Hz)  
snare vol *num* (volume 0 -1)  
snare sample *filepath* (load a sample, omit the .wav extension)  

## Closed Hat  
hhc all (play all 16ths)  
hhc none (play nothing)  
hhc vol *num* (volume 0 -1)  
hhc del *0 - 5000* (delay by Ms)  
hhc binary *0 0 1 0 0 0 1 0* (binary pattern 8 steps)  
hhc offset *0-8* (offset pattern)  
hhc mod *0-8* (length of sequence)  
hhc sample *filepath* (load a sample, omit the .wav extension)  

## Open Hat  
hho play *num* (step of sequence to play)  
hho mod *num* (length of sequence)  
hho hp *num* (high pass filter in Hz)  
hho vol *num* (volume 0-1)  
hho sample *filepath* (not yet implemented)  
hho sample *filepath* (load a sample, omit the .wav extension)  

## Euclidean Clap  
clap mod *0-16* (length of sequence)  
clap steps *0 to above mod* (number of steps to fill)  
clap offset *0 to above mod* (offset pattern)  
clap bit *0-16* (bit crush 1-16bits)  
clap vol (volume 0-1)
clap sample *filepath* (load a sample, omit the .wav extension)  
  
## Bass Synth
bass notes *0 0 3 4 12 7 3 4* (Sequence of 8 notes in chromatic scale)  
bass pitch *num* (pitch with 0 as index)  
bass attack *num* (attack of AD envelope)  
bass decay *num* (decay of AD envelope)  
bass pow (logarithm on envelop decay ramp)  
bass patt *0-255 0-255* (decimal number converted to 8 bit binary gate pattern)  
bass pattmod *0-16* (length of gated pattern for envelop trigger)  
bass notesmod *0-8* (length of note sequence)  
bass lp *num* (low pass filter in Hz)  
bass hp *num* (high pass filter in Hz)  
bass vol (volume 0-1)  
  
**Note:** *loading custom samples*  
When laoding a sample you do not include the filename extension.  
* The .wav extension will automatically be added.  
* E.g. *clap sample user/newclap* will load user/newclap.wav
