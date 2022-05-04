# RePLIA

* [BACK_TO_TOP](./README.md)





##  RePLIA
An open-source high-frequency lock-in amplifier

* [Review of Scientific Instruments: An open-source high-frequency lock-in amplifier](https://aip.scitation.org/doi/10.1063/1.5083797)
    * [LOCAL_COPY](./An_open-source_high-frequency_lock-in_amplifier_1.5083797.pdf)

> ... In this article, we detail an LIA which we have implemented on the STEMlab’s FPGA chip, along with open source29 operational and data transfer software developed specifically for this application. We demonstrate that this device shares many capabilities with more expensive alternatives such as a sweepable internal signal generator, single or dual input/output modes, wave form control, and the ability to increase the number of available inputs and outputs by interfacing across multiple STEMlab units. ...

----
RePLIA Top level diagram

/>
<img
src="img/19.PNG"
width = 900
/>
</p>

----
RePLIA image for the Redpitaya is 3.9 GB
/>
<img
src="img/20.PNG"
width = 900
/>
</p>

----

### nikos review
* RePLIA published at 2019
* Up to 50 MHz
* 90 nV/√Hz of input noise
* Creative Commons Attribution 
* The RePLIA has been used for magnetometry
* Power consumption: 4W when idle and <6W during lock-in operation

### How to emulate a noisy input
* nV/√Hz = nanovolt per root Hertz: Spectral noise density

## Preparing the SD-CARD
RePLIA image for the Redpitaya is 3.9 GB
<p align="center">
<img
src="img/23.PNG"
width = 700
/>
<img
src="img/24.PNG"
width = 700
/>
</p>



## Connecting to RP
* [Connect to Red Pitaya](https://redpitaya.readthedocs.io/en/latest/quickStart/first.html)

connected to rp-f08f57.local/

<p align="center">
<img
src="img/25.PNG"
width = 900
/>
</p>

RePLIA is not accessed from the browser menu, but from command line via ssh, or with the RePLIA GUI (RePLIA control application)

----

## RePLIA Control application
This is the java aplication running in my windows10 PC. It is not connected (yet) to RedPiya.
<p align="center">
<img
src="img/26.PNG"
width = 500
/>
</p>

### How I made the RePLIA Control application RUN
> * Cloned [RePLIA github](https://github.com/WarwickEPR/RePLIA)
> * Created a dos batch file named run.cmd with content   
> `java -jar LIAControl.jar`
> * Updated Java 
> * Added java to the PATH environmental variable: This [HOW TO](https://www.geeksforgeeks.org/how-to-set-java-path-in-windows-and-linux/) helped me
> * Call the run.cmd from command prompt

### Connect the RePLIA controll application to RedPitaya
* We need to convert the domain name rp-xxxxxx to IP addresss.
* I made that by hovering the mouse over the Geotool icon (small greenish circle icon)
<p align="center">
<img
src="img/27.PNG"
width = 900
/>
</p>

----
Connected and setup is sent to RedPitaya
<p align="center">
<img
src="img/28.PNG"
width = 500
/>
</p>

----

When the Apply button is pressed a command line is executed as below:
<p align="center">
<img
src="img/30.PNG"
width = 900
/>
</p>

### Verify we are using the correct IP address
The file config.cfg is created after the Apply button is pressed. Using a wrong IP address the config.cgf file is not affected, so this is a way to confirm we are using the correct IP address
<p align="center">
<img
src="img/29.PNG"
width = 200
/>
</p>

----

## Connect with Putty

> ... the default user and password are 'root' and 'nvmag'
<p align="center">
<img
src="img/31.PNG"
width = 600
/>
</p>

## Start RePLIA
The comand `./startall.sh` starts the RePLIA, and even though there are some Python error messages, it seems the RePLIA is working:
* Orange LEDs appear as a binary counter clocked at 1Hz
* OUT2 has a sawtooth signal at frequency 1Hz
<p align="center">
<img
src="img/32.PNG"
width = 600
/>
</p>


## First day testing conclusions
- Tested using the provided sd-card image
- RePLIA software inside RedPitaya starts, but reports Python error
- [ ] Find a RepLIA video
- Some indication it works
- Can't make it (yet) to output the reference signal, only the scan sawtooth
- [ ] To understand better the `MODE` of operation and the 14 bits that controll the mode
- GUI to be verified it communicates with the board

