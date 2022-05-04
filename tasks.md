[![](https://img.shields.io/badge/organization-The--101--project-blue.svg)](https://github.com/The-101-project) 
[![](https://img.shields.io/badge/remote-Lock_In_Amplifier_Review-green.svg)](https://github.com/The-101-project/LockInAmplifierReview) 
[![](https://img.shields.io/badge/local-F:\prj\electronics\Lock_In_Amplifier_Review-orange.svg)](https://github.com/soldering-channel)

# tasks

* [BACK_TO_TOP](./README.md)


## Generic
- [x] move Redpitaya content from readme to RadPitayaLIA
- [x] Add images
- [x] Add some conclusions

- [ ] Find the meaning of 90 nV/√Hz and how to emulate that

## RePLIA
- [x] Solve the large image for RP sd-card download issue
- [ ] Find the frequency resolution for RePLIA
- [ ] Compare RePLIA with other RedPitaya LIA solutions
- [x] Backup `RP_Lock-in_copy.img` 3.9GB file
- [x] Backup Start testing RePLIA
- [ ] Make a list with first test results on RePLIA


## Orders
- [ ] Order more Redpitaya boards
- [ ] Order Redpitaya compatible WiFi dongles
- [ ] Order RedPitaya connectors

## Testing
- [x] Find the Ethernet cable
- [x] **Test Redpitaya with Ethernet cable connection to router**
- [ ] Test with Redpitaya oscilloscope, the Lock-In method
- [ ] Connect to Red Pitaya with Putty
- [ ] **Add a button to control LED** [LED](https://redpitaya.readthedocs.io/en/latest/developerGuide/software/build/webapp/webexamples/addLEDbut.html)

##  The Lock-in+PID application
- [ ] Test the [The Lock-in+PID application for Red Pitaya](https://marceluda.github.io/rp_lock-in_pid/TheApp/instruments/instruments_01_intro/)
- [ ] View [marcelo luda videos](https://www.youtube.com/c/marceloluda/videos) on Lock-in+PID
- [ ] Check RedPitaya  [Bazaar](https://bazaar.redpitaya.com/) for LIA related applications
    - Oscilloscope+Lock-in+PID (0.1-3) is here too
- [x] Create a new lock-in-pid.md
- [ ] review [rp_lock-in_pid Derivated versions](https://marceluda.github.io/rp_lock-in_pid/Derivated/)
- [ ] Download the papers mentioned in [Lock-in+PID](https://marceluda.github.io/rp_lock-in_pid/)

## Xilinx Vivado 
- [ ] View Xilinx Vivado related video [Tutorial 01 How to do Bare Metal Programming with Red Pitaya](https://www.youtube.com/watch?v=XJbEn_-hjYc)

## Programming

- [ ] Review [programming examples](https://redpitaya.readthedocs.io/en/latest/appsFeatures/remoteControl/remoteControl.html#examples)


## Other RP LIA
- [ ] Review this **verilog LIA** [ ahesse93/RedPitaya_LockInAmplifier](https://github.com/ahesse93/RedPitaya_LockInAmplifier)
- [ ] Review [github lock-in-amplifier ](https://github.com/topics/lock-in-amplifier)  projects

- [ ] Review (Argentina) [Compact embedded device for lock-in
measurements and experiment active control](https://notablesdelaciencia.conicet.gov.ar/bitstream/handle/11336/147988/CONICET_Digital_Nro.dfbb06a5-b662-4027-9879-b046969bd6a8_A.pdf?sequence=2&isAllowed=y)

## PyRPL
- [ ] Review [PyRPL](https://pyrpl.readthedocs.io/en/latest/) with focus to Lock In Amplifiers
- [ ] Also [https://github.com/lneuhaus/pyrpl](https://github.com/lneuhaus/pyrpl)
- [ ] Review if PyRPL has only 1Hz accuracy [Improvements to my Lock in Amplifier implementation with PyRPL](https://forum.redpitaya.com/viewtopic.php?t=23120)
- [ ] Review PyRPL IQ module here [api  IQ module](https://pyrpl.readthedocs.io/en/latest/api.html#module-pyrpl.hardware_modules.iq)
- [ ] Review [First attempts at locking](https://pyrpl.readthedocs.io/en/latest/user_guide/tutorial/#First-attempts-at-locking)

----

- [ ] Review https://github.com/ahesse93/PyRPL-Modification
- [ ] View Interferometer video with PyRPL
- [ ] Review https://github.com/lneuhaus/pyrpl
- [ ] Review https://pyrpl.readthedocs.io/en/latest/

## PSPRT
- [ ] **Make a simple diagram for the QEPAS LIA operation**
   - [x] Review my Markdown notes
        - [x] Review PSPRT reports
        - [x] LIA Reference signal output: Sinousiodal
        - [x] Frequency resolution: 0.1 Hz 
        - [x] Frequency resolution: best  possible 0.011hZ
        - [X] Resonance QEPAS: 12448Hz
        - [x] LPF: 2.5Hz
        - [x] Measurement time for each frequency: 100ms
        - [x] Ramp period: for 1800 points arount resonance--> 3min (1800points x 0.1s = 180s)
        - [ ] Modulation
- [ ] Ask DAC/ADC board schematic