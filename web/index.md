---
keywords: metal, groove, beats, beat tracking, tempo, beat, drums, percussion, percussive, headbang, rhythm, metronome, polyrhythm, multimeter
description: "What makes metal groove? An exploration of beat tracking, tempo estimation, percussive source separation, and various music analysis algorithms for rhythm."
---

# What makes Metal Groove?

I'm Sevag, and for many years I've been obsessed with metal, the genre of music. The best part about metal is the groove: when your head bops uncontrollably, when the moshpit starts cooking.

This page showcases a collection of my loosely-related projects in the pursuit of the analysis of groove and rhythm. See my [open-source portfolio](https://github.com/sevagh) and my [personal website](https://sevag.xyz) for any inquiries.
<br style="line-height:0px;" />

## Motion and percussion-aligned beat tracking

headbang.py: [site](https://sevagh.github.io/headbang.py), [repo](https://github.com/sevagh/headbang.py)

Calculating groove from tempo agreement between auditory beat and motion tempo of drummer's right arm:
{% include embed-video.html src="assets/video/anup_sastry_pose.webm" %}

Calculating groove from tempo agreement between auditory beat and motion of guitarist's head:
{% include embed-video.html src="assets/video/bb_short.webm" %}

Motion-aligned beat tracking:
{% include embed-audio.html src="assets/audio/anup_sastry.ogg" %}

Percussion/onset-aligned beat tracking:
{% include embed-audio.html src="assets/audio/badthing_hbt.ogg" %}

<div style="height:20px;font-size:1px;">&nbsp;</div>

## Polyrhythmic metronome and a drum machine

Libmetro: [site](https://sevagh.github.io/libmetro), [repo](https://github.com/sevagh/libmetro)

C++ metronome library for creating arbitrary click tracks with support for polyrhythm and multiple representations, using [STK](https://github.com/thestk/stk) for drum sound synthesis:

Intuitive format for a 5/3 beat:
```
1 0 0 1 0 0 1 0 0 1 0 0 1 0 0
1 0 0 0 0 1 0 0 0 0 1 0 0 0 0
```
Audio:
{% include embed-audio.html src="assets/audio/poly_53.ogg" %}

A beat given to me by a jazz vibrophonist: 3/5, 5 as a swing pattern
```
1 0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 0 0 1 0 0 0 0
1 0 0 1 0 1 1 0 0 1 0 1 1 0 0 1 0 1 1 0 0 1 0 1 1 0 0 1 0 1
```
Audio:
{% include embed-audio.html src="assets/audio/poly_35_swing.ogg" %}

drum_machine ([repo](https://github.com/sevagh/drum_machine)): Go wrapper for libmetro to generate metronomes from the rhythm information for songs in the [Harmonix Set](https://github.com/urinieto/harmonixset)

<div style="height:20px;font-size:1px;">&nbsp;</div>

## Beat-driven visual animation on Android

ElectroPARTYogram: [repo](https://github.com/sevagh/ElectroPARTYogram)

Tempo and beat-driven animation in an Android app, powered by [BTrack](https://github.com/adamstark/BTrack) and animated with [SFML](https://www.sfml-dev.org/), with visualization intensity influenced by onset strength:
{% include embed-video.html src="assets/video/animals_as_leaders_the_woven_web.webm" %}
<div style="height:20px;font-size:1px;">&nbsp;</div>

## Music demixer, stem, and source separation

Music Demixer

## Source separation and percussion enhancement utilities

* "Music Demixer", my free and paid websites and Android app that offer private, offline Demucs:
    * <https://freemusicdemixer.com>
    * <https://pro.freemusicdemixer.com>
    * <https://play.google.com/store/apps/details?id=com.freemusicdemixer.pro>

Here are some samples of the very high quality source separation performance of my Pro Deluxe model applied to a Periphery song:

While working on headbang.py, I dug deep into the field of source separation (aka stem separation, music demixing, stem isolation). While not directly related to metal, groove, or rhythm, isolating the percussion in a song can be a key step in performing further percussion analysis.

* Transient shaper/percussion enhancement: [multiband-transient-shaper](https://github.com/sevagh/multiband-transient-shaper)
* Realtime harmonic-percussive source separation: [Real-Time-HPSS](https://github.com/sevagh/Real-Time-HPSS), [Zen](https://github.com/sevagh/Zen)
* Analysis of simple and complex source separation algorithms from the angle of time-frequency: [Music-Separation-TF](https://github.com/sevagh/Music-Separation-TF)
* Custom source separation AI models: [MiXiN](https://github.com/sevagh/MiXiN), [xumx-sliCQ](https://github.com/sevagh/xumx-sliCQ)
* Custom C++ inference for PyTorch source separation models: [umx.cpp](https://github.com/sevagh/umx.cpp), [demucs.cpp](https://github.com/sevagh/demucs.cpp)

