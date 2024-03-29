# RedPitayaLIA

* [BACK_TO_TOP](README.md)

----

<!-- @import "[TOC]" {cmd="toc" depthFrom=1 depthTo=6 orderedList=false} -->

<!-- code_chunk_output -->

- [RedPitayaLIA](#redpitayalia)
  - [Red Pitaya Lock In](#red-pitaya-lock-in)
  - [Red Pitaya LIA options](#red-pitaya-lia-options)
    - [1. Lock-in+PID](#1-lock-inpid)
    - [2. An open-source high-frequency lock-in amplifier](#2-an-open-source-high-frequency-lock-in-amplifier)
    - [3. PyRPL](#3-pyrpl)
    - [4. Linien](#4-linien)
      - [My testing with Linien](#my-testing-with-linien)
  - [Links](#links)

<!-- /code_chunk_output -->

 ## Red-Pitaya overview
 
 FPGA board with XILINX at €300, with integrated `[125MHz 14bit ADC] & [125MHz 14bit DAC]`
   * Designed to be used as a low cost and high performance measurening instrument (oscilloscope, analyzers, etc...)
   * Evaluate/Use open source LIA firmware
   * Scientific community and publications
   * Python control via a host
   * A variety of Python libraries
   * Instrument type interfaces PyVISA and more
   * *The effort to create a LIA instrument, is focused to PC Software engineering*
   * [SCPI server (MATLAB, LabVIEW, Scilab or Python)](https://redpitaya.com/rtd-iframe/?iframe=https://redpitaya.readthedocs.io/en/latest/appsFeatures/remoteControl/remoteAndProg.html)

## Red Pitaya Lock In

Most open source FPGA LIA implementations today (Feb 2022) seem to be based on the Red Pitaya, and specifically on the board [stemlab-125-14](https://redpitaya.com/stemlab-125-14/), which at [RS](https://ie.rs-online.com/web/p/oscilloscopes/1271086) costs €288.00 (€354.24 inc. VAT). RP is used in Scientific publications on Laser spectroscopy...


* [RS Red Pitaya products](https://uk.rs-online.com/web/b/Red-Pitaya/?cm_mmc=IE-PPC-DS3A-_-google-_-2_IE_EN_Suppliers_Red+Pitaya_Exact-_-Red+Pitaya_Pure-_-red+pitaya&matchtype=e&kwd-23777362289&gclid=Cj0KCQiA09eQBhCxARIsAAYRiynxqvpv4DSHIqQS35pyoZMyPBrtmIszIfYnIXlHKd1gOTzV2A6V3f8aArHlEALw_wcB&gclsrc=aw.ds)
* [at elektor](https://www.elektor.com/stemlab-125-14-starter-kit)
* [3D models](https://redpitaya.readthedocs.io/en/latest/developerGuide/hardware/mechSpec.html)


----



## Red Pitaya LIA options

### 1. Lock-in+PID
* A complete instrument: Open source XILINX code and PC Python? Software. 
* This is the easiest to install and test, as it is available in RP market-place 

* [Red Pitaya Lock-in+PID Application](https://github.com/marceluda/rp_lock-in_pid/)
* [Lock-in+PID](https://marceluda.github.io/rp_lock-in_pid/)

### 2. An open-source high-frequency lock-in amplifier
* [An open-source high-frequency lock-in amplifier](https://aip.scitation.org/doi/10.1063/1.5083797) 

### 3. PyRPL
* [PyRPL](https://pyrpl.readthedocs.io/en/latest/)  turns your RedPitaya into a powerful DSP device, especially suitable as a digital lockbox and measurement device in quantum optics experiments

### 4. Linien
User-friendly locking of lasers using RedPitaya (STEMlab 125-14) that just works
* [linien](https://pypi.org/project/linien/) User-friendly locking of lasers using RedPitaya (STEMlab 125-14) that just works
* [linien github](https://github.com/linien-org/linien)
* [Cornell](https://arxiv.org/abs/2203.02947)
* [Linien project metrics](https://kandi.openweaver.com/python/hermitdemschoenenleben/linien#Summary)

----
#### My testing with Linien
<p align="center">
<img
src="img/40.PNG"
width = 500
/>
</p>

```
I just installed linien to RP.

I start having some understanding on what is the meaning of ‘Spectroscopy’
It seems they always sweep the reference to a wide range. Linien goes up to 50MHz

We can’t have a static reference, and we cant set a sweep range (??)
The modulation frequency can be set.
Demodulation can be set 1,2,3,4,5 x Reference
Filter can be down to 1Hz, not lower.

If I understand correctly this way of operation is not useful for us
We want to be able to control the Reference.

But if you have time to read the documentation, you  might be able to understand better?`

```

* Exported Linien configuration json
```
{"linien-version": "0.5.3", "time": 1652376355.2368507, "parameters": {"fast_mode": 0, "modulation_amplitude": 8191.5, "modulation_frequency": 100663.296, "sweep_speed": 8, "demodulation_phase_a": 0, "demodulation_multiplier_a": 2, "demodulation_phase_b": 0, "demodulation_multiplier_b": 1, "offset_a": 8191.0, "offset_b": 0, "invert_a": false, "invert_b": false, "filter_1_enabled_a": 1, "filter_1_enabled_b": false, "filter_1_frequency_a": 1, "filter_1_frequency_b": 10000, "filter_1_type_a": 0, "filter_1_type_b": 0, "filter_2_enabled_a": 1, "filter_2_enabled_b": false, "filter_2_frequency_a": 1, "filter_2_frequency_b": 10000, "filter_2_type_a": 0, "filter_2_type_b": 0, "filter_automatic_a": 0, "filter_automatic_b": true, "p": 50, "i": 5, "d": 0, "watch_lock": true, "watch_lock_threshold": 0.01, "dual_channel": false, "channel_mixing": 0, "pid_on_slow_enabled": false, "pid_on_slow_strength": 0, "mod_channel": 0, "control_channel": 1, "sweep_channel": 1, "polarity_fast_out1": false, "polarity_fast_out2": false, "polarity_analog_out0": false, "check_lock": true, "analog_out_1": 0, "analog_out_2": 0, "analog_out_3": 0, "plot_line_width": 2, "plot_color_0": [200, 0, 0, 200], "plot_color_1": [0, 200, 0, 200], "plot_color_2": [0, 0, 200, 200], "plot_color_3": [200, 200, 0, 200], "plot_line_opacity": 230, "plot_fill_opacity": 70, "autolock_determine_offset": true, "autolock_mode_preference": 0, "psd_acquisition_max_decimation": 18}}
```

----










## Links

  * [Can anyone give me a laymans explanation of the "nV/rtHz" specification/measure?](https://www.eevblog.com/forum/chat/can-anyone-give-me-a-laymans-explanation-of-the-_nvrthz_-specificationmeasure/)
  * [NOISE ANALYSIS - RESISTOR EXAMPLE](http://www.ecircuitcenter.com/Circuits/Noise/Noise_Analysis/res_noise.htm)
* https://www.designnews.com/what-nvvhz-noise
* [snva515c](https://www.ti.com/lit/an/snva515c/snva515c.pdf?ts=1650375636618&ref_url=https%253A%252F%252Fwww.google.com%252F)
* [How can I measure and calculate nV/Root Hz (nanovolt per root Hertz) on a spectrum analyzer?](https://www.tek.com/en/support/faqs/how-can-i-measure-and-calculate-nv-root-hz-nanovolt-root-hertz-spectrum-analyzer)