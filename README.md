About the <h1>Audio Upskiling</h1>

<h2>Audio Signal Processing</h2>
<h4>Application</h4>
1. Audio Classification
2.

Content
Sound waves
DAC/ADC
Time and frequecngy domain audio frequecny
Audio transformation
    Fourier Transform
    Constant-Q Transform
    Mel Spectrograms
    Chromograms


Theory + Coding

https://github.com/musikalkemist/AudioSignalProcessingForML/tree/master/1-%20Overview

python library
librosa

understand data
familirase frequenvy/time domai audio features
extract featurs from audio
reconize audio feature in ml application
preporcess audio  data
math for audio transform
librosa use

sound
produce by vibration of matter
vibration cause air molecules to oscillate
change in air pressure creates a wave

Mechanical wave
oscillation that travels through space
energy travels from one point to another
the medium is deformed

atmospheric pressure
compression -> denser part
rarefracttion -> thin part

wavefrom
frequency
intensity
timbre

periodic(single sinewave, multiple sinewaves) and aperiodic sound(noise, pulse)

waveform
y(t) = Asin(2pift+fi)
f -> frequency -> inverse of timeperiod -> ertz
A -> amplitude
fi -> phase

higher frequency -> higher sound
larger amplitude -> louder sound

hearing range
20hz-20khz -> human

pitch
logarithtmic perception
2 frequencies are perceived similarly if they differ by a power of 2

Midi notes
A3 - 220hz
pich 69 -> A4 - 440hz
A5 - 880hz

mapping pitch to frequency
F(p) = 2^((p-69)/12)*440
F(p+1)/F(p) = 2^(1/12) = 1.059

cents
octave is divided into 1200 cents
100 cents in a semitone
noticeable pitch difference:10-25 cents

Intensiy, loudness and timbre

sound power
rate at which energy is transferred
energy per unit time
