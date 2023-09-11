# whose-chaos-modules
Unstable, Non-Linear and Chaotic Sound Modules for Pd.

<img width="481" alt="Screenshot 2023-09-11 at 17 15 45" src="https://github.com/whosebodyisthis/whose-chaos-modules-v0.3/assets/133358060/7f8dd49c-3634-48c0-b9e4-c7cf61e05976">


whose's-chaos-modules (Pd) (v0.3)
========================================

This package contains a set of vanilla Pd abstractions focused on the concept of unstable,
chaotic and dynamical systems. 


Requirements:
=============
- At least Pd Version 0.52-x (may work in older versions, but not recommended)

I also highly recommend solidpd's AudioLab externals as utilities for audio out,
file recording and EQ'ing, they are available here: https://github.com/solipd/AudioLab

This package contains many abstracions, however, not all are intended to be used as patchable 
objects. Below is a list of all 'instruments' and control modules in this package:


Instruments:
============
[w.feedbacker1~] - Non-Linear, stereo feedbacking module.

[w.chuapet~] - Unstable Chua oscillator, with self-wavefolding.

[w.hillary~] - Controllable Duffing oscillator, with resonant bandpass array tuned to Bark scale.

[w.hillary2~] - Controllable Duffing oscillator, with constant skirt-gain bandpass array, tuned to Bark scale.

[w.choreographer] - Dynamic score generator control module, generating 6 'systems' to control other modules.

[w.lfo~] - Control-rate low frequency oscillator.

[w.thumper~] - Triggerable AHR envelope.

[w.resonbp~] - Constant skirt-gain bandpass filter. Q controls resonance-peak decay time.

[w.benjolin~] - Recreation of Rob Hordijk's 'Benjolin'.

[w.benjola~] - Imitation/approximation of Rob Hordijk's Benjolin/Rungler. Goes crazy in 'chaos' mode.

[w.sampler1~] - Stereo, varispeed sampler, with momentary record function.


How to install:
=====
Download this package from github.

Move the folder into a convinient location 

Download Pd if you haven't already and open it

In Pd, "Preferences -> Path" and add where you put this folder

You should now be able to add these objects in any Pd patch using "CMD/CTRL+1" and typing the name of an instrument.

NEW Preset System:
==================
As of version 0.3, all modules have a preset recall and save system. Each module can hold 8 presets by default.
Choose a preset with the small black box towards the top of the UI.
Click the 'wrt' bang to write a preset into the selected bank.
Click 'lod' to recall the current preset.
Preset 1 will be loaded by deafult upon object creation.

About modules:
==============
If a module has multiple inlets, the rightmost inlet is always used for modulation sources: use it by having a message box
with the first arugment as a slider name (e.g., delay_ms from [feedbacker1~]), followed by $1, with a CONTROL-RATE 
modulation source going into the message box. 

Multiple modulations can use the same inlet. Other inlets may be control data, or more commonly audio-rate inputs. 

You may refer to the _'EXAMPLE-PATCH.pd'_ for an immediate demonstration of some modules, how they can be patched and controlled.

If you modify or use these abstractions, please let me know! I'd love to hear what people are doing with them.

Feel free to contact me (whosebodyisthis@gmail.com or @whosebodyisthis on Instagram) for help with any of this
this stuff.
