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

Threshold of hearing
human can perceive sounds with very small intensities
TOH = 10e-12W/m^2

Threshold of pain
TOP = 10 W/m^2

Intensity level
lograthmic scale
measured in decibels(dB)
ration between two intensity value
use an intensity of reference(TOH)

dB(I) = 10log(I/I(TOH))
0 dB means I = I(TOH)

Every ~3dB, intensity double

Loudness
subjective perception of sound intendity
depends on duration/frequency of sound
depends on age
measured in phons

Timbre
colour of sound
diff between two sounds with same intensity, frequency, duration
described with words like: bright,dark, dull, harsh, warm

Features of timbre
timbre is multidimensional
sound envelope
harmonic conttent
amplitude/ frequency modulation

Sound envelope
Atttac-Decay-sustatin-Release

Complex sound
superposititon of sinusoids
A partial is a sinusoid used to describe a sound
a lowestt partial i calld fundamental frequency
a harmonic partial is a frequency that's a multiple of the fundamental frequency
f1=440, f2=80, f3=3*440
inharmonicity indicates a deviation

frequency modulation
aka vibrato
periodic vibration in frequency

Understanding audio singal
analog signal
continuous signal

digital signal
sequence of discrete value

Analog to digital conversion
Sampling
Quantization

audio digital signal -> pulse-code modulation

high sample rate -> less sampling error
low sample rate -> high sampling error

Nyquist frequency
sr >= 2f(nyquist frequency)

sampling
sampling on x-axis

Quantization
sampling on y-axis
resolution = num of bits
bit depth
cd resolution = 16 bits

memory for 1min sound
sr = 44100hz
bit depth = 16

16*44100 / 1048576/8  * 50 = 5.49MB

Dynamic range
diff between largest/smallest sigal system can record
high resolution -> high dynamic range


signal to quantization noise ratio
relationship between max signal strength and quantization error
correlates with dynamic range
sqnr(16) ~ 96dB

how to record sound?
source ->ADC -> comptetr


Audio features
Description of sound
differentt featurs caputtre differentt aspects of sound
built intelligent audio system

audio feature cattegorisation
level of abstraction
temprol scope
music aspec
signal domain
ml approcah

level of abstraction
high -> understand like instrumentation, keyy, chord, melody, tempo, lyrics, genre
mid -> make sense for human like pitc, beat, note onsets, fluctution patterns
low -> makes sense for machine usually not for human

temporal scope
instanteous -> give information in less time or instant
segment-level -> give information about musical phrase information form longer period
global -> aggregration of the result that descrbe the whole sound

music aspect
beat
timbre
pitch
harmony

signal domain
time domain -> amplitude envelope, root-mean square energy, zero crossing rate
frequency domain -> band energy ratio, spectral centroid, specttral flux
time-frequency representation -> spectrogram mel-specttrogram , constant-q-transform

machine learning approach
tradinal machine learning ->  amplitude envelope**, root-mean square energy, zero crossing rate**, band energy ratio, spectral centroid, specttral flx**, spectral spread, spectral roll-off
** ==> traditional ml algorithm ==> 'prediction'
deep learning  ->


TYpes of inelligent audio system
DSP --> rule base system
traditional --> feature engineering
deep learning --> automatic feature extraction
