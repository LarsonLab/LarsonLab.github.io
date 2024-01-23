---
layout: post
title:  "The Sounds of MRI"
author: peder
categories: [ fun ]
image: assets/images/The%20Sound%20of%20MRI.jpg
featured: true
---
When I tell people I work on MRI systems, one of the most common questions is about the sounds (or maybe described as noise, depending on your experience).  Why is it so loud?  Can you make it quieter?

Jump to the bottom of the article if you just want to hear MRI machines making music

## What causes the sounds of MRI?

The sounds made during an MRI scan are primarily due to the magnetic field gradient coils.  It occurs when the coils are switched on and off in the presence of a magnetic field (in MRI, the main B0 field).  When the currents inside these coils are changed, there is a force exerted on the coils.  This is called the Lorentz force, which is a force that is exerted on a charged patricle (currents) in a magnetic field.  

The pitch or frequencies created during the scan depend on the rate that the gradient coils are turned on and off.  For example, to get middle C (440 Hz), the gradients should be switched at a rate of 1/440 Hz = 2.2 ms.

## Sounds and the Pulse Sequence

Different pulse sequences have very different patterns, depending on the overall timing as well as the rate of gradient switching rates.

Echo-planar Imaging (EPI) is a great example, as it is typically done with the most rapid gradient switching possible.  The switching rates is often less than 1 ms, leading to frequencies of 1 kHz and above.  EPI readouts are also short (< 100 ms) which then leads to high frequency "chirps".

![Echo planar imaging (EPI) sequence](../assets/images/EPI%20sequence.jpg)

Diffusion-weighting gradients are another great as example, as they have some of the longest gradient pulse durations and thus slow switching rates.  But they are also very high amplitude so have a strong volume.  Thus diffusion-weighting leads to very low frequency sounds, in my experience to the point you feel the vibration in the table and your bones.  In a diffusion pulse sequence, where $\Delta$ is typically 10-50 ms, leading to frequencies of 100 Hz and below.

![Diffusion Pulse sequence, where $\Delta$ is on the order of 10s of ms](../assets/images/Spin-echo%20diffusion%20sequence.jpg)

Given these patterns, you can identify some characteristics of the pulse sequence while you are being scanned.  Some examples
* repeated high frequency patterns would indicate an EPI readout, e.g. for DWI or fMRI
* consistent, moderate frequency (a bit grinding) is probably a T1-weighted (short TR) scan
* large gaps in sound indicate long TR, for example in T2 weighted imaging
* other unqiue sequence timings are distinct, such as inversion recovery which is a blip (crusher gradient after inversion pulse), delay, up to 1 s of noise (readout), and another delay

You can find sounds recorded for a full MRI exam here: <https://www.youtube.com/watch?v=TIsrOtSSUQY>

## Making Quieter MRI scans

Since the sounds in MRI are caused by the changing of the magnetic field gradient currents, a MRI scan can be made quieter by reduced the rate at which the gradients are changed.  However, this is much easier said than done, as many MRI scans rely of rapid switching of these gradients to create contrast, to get high SNR, and/or to keep scan times from getting too long.

The most prominent example of quieter MRI scans I'm aware of are zero echo time (ZTE) pulse sequences.  I have worked with these sequences and it is shocking - you expect to hear the scanning easily from outside the room, but instead you have to strain and maybe turn up the scan room microphone volume to even hear the sequence!

These work by having the gradients on prior to the RF pulse so the k-space trajectory begins immediately.  Data is read out, and then the gradients are only slightly changed for the next repetition.  This slow change in the gradients is the key feature that makes them silent.

![ZTE Pulse Sequence](../assets/images/ZTE%20pulse%20sequence.jpg)

More info:

Ljungberg, E., Damestani, N.L., Wood, T.C., Lythgoe, D.J., Zelaya, F., Williams, S.C., Solana, A.B., Barker, G.J. and Wiesinger, F., 2021. Silent zero TE MR neuroimaging: current state-of-the-art and future directions. Progress in Nuclear Magnetic Resonance Spectroscopy, 123, pp.73-93. <https://doi.org/10.1016/j.pnmrs.2021.03.002>

## The Most Annoying MRI Scan

My team happens to work with one of the arguably most annoying sounding MRI scans.  It is a 3D ultrashort echo time (UTE) sequence, basically a T1-weighted scan with a short TR, but with the twist that the gradient direction is being incoherently modified every TR.  This leads to an extremely dissonant set of frequencies when the scanner is running

[3D radial UTE sequence with golden angle ordering](../assets/audio/UTE%20golden%20spaceship.wav)

[3D radial UTE sequence with bit-reversed ordering](../assets/audio/UTE%20reverse%20spaceship.wav)


## Making Music with MRI

Some clever MRI experts have realized that we can do a reasonable job at controlling the sounds that are created by a MRI scanner.

There are fun examples of playing songs on a MRI scanner (a pretty expensive instrument!).  
* This example uses the MRI scanner for the iconic guitar riff in Smoke on the Water by Deep Purple: <https://www.youtube.com/watch?v=CH9f8tcMAIQ>
* The XX - Intro - MRI Cover, with some nice visualization as well: <https://youtu.be/XX0UGblIwMM?si=tas3EAz_aQtmNmA9>
* There is another beautiful example of MR fingerprinting, a quantitative imaging technique, making music while actually also producing good quality data:

Ma, D., Pierre, E.Y., Jiang, Y., Schluchter, M.D., Setsompop, K., Gulani, V. and Griswold, M.A. (2016), Music-based magnetic resonance fingerprinting to improve patient comfort during MRI examinations. Magn. Reson. Med., 75: 2303-2314. <https://doi.org/10.1002/mrm.25818> 

[Bach's Cello Suite No. 1, based on a recording by Yo-Yo Ma, played on a MRI scanner](https://onlinelibrary.wiley.com/action/downloadSupplement?doi=10.1002%2Fmrm.25818&file=mrm25818-sup-0006-suppinfo06.mp3)
