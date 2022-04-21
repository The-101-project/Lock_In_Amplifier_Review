
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

## Digita PSD vs Analog PSD
The amplified signal is converted to digital
form using a 16-bit A/D converter sampling at 256 kHz. The
A/D converter is preceeded by a 102 kHz anti-aliasing filter to
prevent higher frequency inputs from aliasing below 102 kHz
### 16-bit A/D converter sampling at 256 kHz

### 102 kHz anti-aliasing filter

### Multiplier 

#### Sample every Every 4us
#### Multiply by both reference sines