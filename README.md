# Tiny Techno Pseudo Language 
*Superceded by Garden but i guess this is still good for Techno*  

Tiny Techno Pseudo language is a live coding tool for minimal techno. It is lightweight, Pure Data based and tiny in size and scope.  
It is a system aimed at rejecting complex structures, in favour of just telling the thing what to do and it does it.

## Installation 
Open main.pd in Pure Data (www.puredata.info)  
In a terminal, navigate to your pd directory.  

Into the /bin folder  

run the following: **pdsend 6000 localhost udp**  

**Then you can control the audio engine with the following commands...**  

## Global  
start *1/0* (start or stop metronome)  
bpm *num* (change bpm)  
  
## Drum Machine
### Kick Drum  
kick play *num* (step of sequence to play)  
kick mod *num* (length of sequence)  
kick dist *0-1* (amount of distortion to apply)  
kick vol *num* (volume 0 -1)  
kick sample *filepath* (load a sample, omit the .wav extension)  

### Snare Drum  
snare play *num* (step of sequence to play)  
snare mod *num* (length of sequence)  
snare lp *num* (low pass filter in Hz)  
snare vol *num* (volume 0 -1)  
snare sample *filepath* (load a sample, omit the .wav extension)  

### Closed Hat  
hhc all (play all 16ths)  
hhc none (play nothing)  
hhc vol *num* (volume 0 -1)  
hhc del *0 - 5000* (delay by Ms)  
hhc bin *0 0 1 0 0 0 1 0* (binary pattern 8 steps)  
hhc offset *0-8* (offset pattern)  
hhc mod *0-8* (length of sequence)  
hhc sample *filepath* (load a sample, omit the .wav extension)  

### Cymbal  
cym play *num* (step of sequence to play)  
cym mod *num* (length of sequence)  
cym hp *num* (high pass filter in Hz)  
cym vol *num* (volume 0-1)  
cym sample *filepath* (load a sample, omit the .wav extension)  

### Euclidean Clap  
clap mod *0-16* (length of sequence)  
clap euc *0 to above mod* (number of steps to occupy)  
clap offset *0 to above mod* (offset pattern)  
clap bit *0-16* (bit crush 1-16bits)  
clap vol *num* (volume 0-1)
clap sample *filepath* (load a sample, omit the .wav extension)  
  
## Bass
bass riff *0 0 3 4 12 7 3 4* (sequence of 8 notes in chromatic scale)  
bass riffmod *0-8* (length of sequence) 
  
bass pattern *0-255 0-255* (decimal number converted to 8 bit binary gate pattern)  
bass patternmod *0-16* (length of pattern for gate pattern)  
bass space *num* (spacing between moving to the next note in the riff)
  
bass attack *num* (attack of AD envelope)  
bass decay *num* (decay of AD envelope)  
bass pow *num* (logarithm on envelope decay ramp)  
  
bass pitch *num* (pitch with 0 as index)    
bass vol *num* (volume 0-1)  
  
bass wave *sqr/sin/saw* (choose oscillator)  
  
## Synthesiser
synth type *fm/loop/dualosc* (choose synth voice)  
  
synth vol *num* (volume 0 -1)  
synth lp *0-20000* (low pass filter)  

synth attack *num* (attack of AD envelope)  
synth decay *num* (decay of AD envelope)  
synth pow *num* (logarithm on envelope decay ramp) 
  
synth riff *0 0 3 4 12 7 3 4* (sequence of 8 notes in chromatic scale)  
synth riffmod *0-8* (length of riff pattern)

synth pattern *0-255 0-255* (decimal number converted to 8 bit binary gate pattern)  
synth patternmod *0-16* (length of pattern for gate pattern)

synth delay *0-1* (delay volume on synth)
synth feedback *0.1 - 0.9* (delay feedback)
  
#### FM Synth
synth fmratio *num* (FM harmonicity ratio)  
synth fmindex *num* (FM modulation index)
  
#### Loop Synth
synth sample *filepath* (load a sample, omit the .wav extension)  
  
#### Dualosc Synth
synth detune *num* (pitch of second oscilator, defaults at 0.99)  
  
  
## Sampler
sampler sample *filepath* (load a sample, omit the .wav extension)  
sampler play *num* (step of sequence to play)  
sampler mod *num* (length of sequence)  
sampler rev (toggle sample reverse - WIP)  
sampler verb *0-100* (reverb level)  
sampler start *0-100* (starting point of playback, 0 is start of wave file)  
sampler vol *num* (volume 0 -1)  

## Mix
mix lp *num* (low pass filter in Hz)  
mix hp *num* (high pass filter in Hz)  
mix verb *0-100* (reverb level)  
mix glitch vol *0-1* (glitch effect volume)  
mix glitch trig (how often to re-trigger glitch loop length)  
mix glitch rec (how often to record a glitch sample)  
mix comb vol *0-1* (comb filter volume)
mix comb tex *1-30* (comb folter texture)

  
**Note:** *loading custom samples*  
The sampler laods into an array, this can cause a slight pause when loading large samples.  
Load large samples first. Small samples are good. Small is always good.  
When loading a sample you do not include the filename extension.    
* The .wav extension will automatically be added.  
* E.g. *clap sample user/newclap* will load user/newclap.wav  
* All samples revert to mono, if a stereo sample is loaded, it will play the left channel.  
  
  
## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.
Please keep in mind the scope of the project is intended to be tiny.
  
Thanks to whoever made the base converter, if i can find out who you are i'll give you a shout out!
  
  
## License
[GNU](https://choosealicense.com/licenses/agpl-3.0/)

