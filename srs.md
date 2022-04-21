
# srs

<p align="center">
<img
src="img/22.PNG"
width = 900
/>
</p>

## PSD
The PSD can detect the signal at 10 kHz with a bandwidth as narrow as 0.01 Hz!
123
### Phase Sensitive Detector 
### @10 KHz BW 0.01Hz

## Low Pass Filter
If the PSD output is passed through a low pass filter, the AC signals are removed.

### AC signals  removed

### DC signal proportional to the signal amplitude.
### The low pass filter bandwidth determines the bandwidth of detection
### Only the signal at the reference frequency will result in a true DC output 

## Magnitude and phase
### 2 outputs: X = Vsigcosθ Y = Vsigsinθ
### magnitude (R) of the signal vector
#### Phase dependency is removed 
#### R = (X2 + Y2)½ = Vsig

## Digital PSD vs Analog PSD
The amplified signal is converted to digital
form using a 16-bit A/D converter sampling at 256 kHz. The
A/D converter is preceeded by a 102 kHz anti-aliasing filter to
prevent higher frequency inputs from aliasing below 102 kHz

The overall performance of a lock-in amplifier is largely
determined by the performance of its phase sensitive
detectors. In virtually all respects, the digital PSD outperforms
its analog counterparts.

### 16-bit A/D converter sampling at 256 kHz

### 102 kHz anti-aliasing filter

### Multiplier 

#### Sample every Every 4us
#### Multiply by both reference sines

### Analog PSD issues
Analog PSDs (both square wave and
linear) have many problems associated with them. The main
problems are harmonic rejection, output offsets, limited
dynamic reserve, and gain error.



#### harmonic rejection
#### output offsets
#### limited dynamic reserve 
####  gain error

### Digital  PSD advantages
Analog PSDs (both square wave and
linear) have many problems associated with them. The main
problems are harmonic rejection, output offsets, limited
dynamic reserve, and gain error.

#### very low harmonic content
Because the reference sine
waves are computed to 20 bits of accuracy, they have very low
harmonic content. In fact, the harmonics are at the −120 dB
level!

#### no erroneous DC output offsets
Output offset is a problem because the signal of interest is a
DC output from the PSD, and an output offset contributes to
error and zero drift. The offset problems of analog PSDs are
eliminated using the digital multiplier. There are no erroneous
DC output offsets from the digital multiplication of the signal
and reference. In fact, the actual multiplication is virtually
error free.

#### limited dynamic reserve 
####  gain error


