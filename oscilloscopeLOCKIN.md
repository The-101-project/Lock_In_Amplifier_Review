[![](https://img.shields.io/badge/organization-The--101--project-blue.svg)](https://github.com/The-101-project) 
[![](https://img.shields.io/badge/remote-Lock_In_Amplifier_Review-green.svg)](https://github.com/The-101-project/LockInAmplifierReview) 
[![](https://img.shields.io/badge/local-F:\prj\electronics\Lock_In_Amplifier_Review-orange.svg)](https://github.com/soldering-channel)


# oscilloscopeLOCKIN

* [BACK_TO_TOP](./README.md)

### Mark Sch video
watched 22 Feb 2022  
Mark Sch Youtube video [Measuring signals buried in noise with an Oscilloscope](https://www.youtube.com/watch?v=vv-xkNa1Z9s&list=PL3Wrg9iIHo1tMckpT1HD4EOCn3QRuW9JZ&index=4)

#### Mark Sch comments
'Using an external reference, all the noise gets averaged out leaving only the signal in phase with the reference. Similar to how a lock in amplifier works.'

<img src="img/11.PNG" width = 800 />

<img src="img/10.PNG" width = 800 />

#### My Summary: 
The value of this technique: **You only need a digital oscilloscope, to start testing/evaluting the Lock In Amplifier  concept**. No LIA needed, but it is not replicating exactly the  LIA operation.  

Steps:   
* `Chanell-1`: Connect the received signal with AC coupling
* `Channel-2`: Connect the reference signal
* Trigger source: `channel-2`
* Average function applied to `channel-1`
* RMS function applied to averaged `channel-1`

### EEVBlog
Thread read 23 Feb 2022  

* [Oscilloscope as a lock-in amplifier (Rigol DS1054Z)](https://www.eevblog.com/forum/projects/oscilloscope-with-trace-averaging-as-a-lock-in-amplifier-(rigol-ds1054z)/)
* book [Lock-in amplifiers: principles and applications (e-edition)](https://www.sites.google.com/site/lockinamplifiers/home)
  * [Local copy](doc/LockinAmplifiersMlMeade.pdf) 

### Nikos experiment 06 March 2022
2 x blue 3mm LEDs, 
* The 1st LED transmitting, connected to the oscilloscope calibration 1KHz generator output
* The 2nd LED receiving from 6cm distance, connected without any amplifier to the Oscilloscope Input

Oscilloscope probes
* Channel-1: Connected to the receiving LED. Set to maximum amplification: **20mV/div**
* Channel-2: Connected to the transmitting LED, 1V/div, the driving signal is 2.8V


<p align="center">
<img
src="img/14.PNG"
width = 500
/>
</p>

----

* Trigger to the Receving LED, channel-1  
RESULT: Too match noise, can't see any receiving signal
<p align="center">
<img
src="img/15.PNG"
width = 500
/>
</p>

----
* Trigger to the Transmitting signal, channel-2  
* RESULT: As above, too match noise, can't see any receiving signal
<p align="center">
<img
src="img/16.PNG"
width = 500
/>
</p>

----
* Trigger to the Transmitting signal: channel-2 
* From the `ACoUIRE` menu, selected: Averaging (channel-1) with 128 samples  

RESULT: **SUCCESS** THE RECEIVER SIGNAL IS 'EXTRACTED FROM NOISE'
* The receiving signal amplitude is 10mV p-p.

<p align="center">
<img
src="img/17.PNG"
width = 500
/>
</p>

----

