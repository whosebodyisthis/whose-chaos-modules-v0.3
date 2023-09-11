CHAOTIC AND UNSTABLE MODULES (Pd) (v0.1)
========================================

This package contains a set of vanilla Pd abstractions focused on the core concept of unstable,
chaotic and dynamical systems. 

REQUIREMENTS:
=============
At least Pd Version 0.52-x (may work in older versions, but not recommended)

This package contains many abstracions, however, not all are intended to be used as patchable 
objects. Below is a list of all 'instruments' and control modules in this package:


[feedbacker1~] - Non-Linear, stereo feedbacking module.
[chuapet~] - Unstable Chua oscillator, with self-wavefolding.
[hillary~] - Controllable Duffing oscillator, with resonant bandpass array tuned to Bark scale.
[hillary2~] - Controllable Duffing oscillator, with constant skirt-gain bandpass array, tuned to Bark scale.
[choreographer] - Dynamic score generator control module, generating 6 'systems' to control other modules.
[lfo~] - Control-rate low frequency oscillator.
[thumper~] - Triggerable AHR envelope.
[resonbp~] - Constant skirt-gain bandpass filter. Q controls resonance-peak decay time.


This package may be added to your Pd search path/externals folder to instantiate objects in any patch, however, this is not 
currently recommended as the naming convention does not yet account for possible naming conflicts if you use
many external libraries. 

You can add the objects mentioned in the list above to any Pd patch, and patch them together in the standard manner.
If a module has multiple inlets, the rightmost inlet is used for modulation sources: use it by having a message box
with the first arugment as a slider name (e.g., delay_ms from [feedbacker1~]), followed by $1, with a CONTROL-RATE 
modulation source going into the message box. Multiple modulations can use the same inlet. Other inlets may be control data,
or more commonly audio-rate inputs. This version does not have a complete set of help files, but subsequent versions 
will have detailed documentation on inlet data types. You may refer to the '_EXAMPLE-PATCH.pd'_ for an immediate 
demonstration of some modules, how they can be patched and controlled.

Feel free to contact me (whosebodyisthis@gmail.com or @whosebodyisthis on Instagram) for help with
this package.