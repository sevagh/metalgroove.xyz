---
keywords: metal, groove, beats, beat tracking, tempo, beat, drums, percussion, percussive, headbang, rhythm, metronome, polyrhythm, multimeter
description: "Beat tracking, tempo estimation, percussive source separation, and other music analysis tools for rhythm in metal music."
---

I'm Sevag and I love metal. This page showcases a collection of my loosely-related projects in the pursuit of the analysis of groove and rhythm in metal music. See my [open-source portfolio](https://github.com/sevagh) and my [personal website](https://sevag.xyz) for any inquiries.
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

## Practice your groove with Music Demixer

"Music Demixer" is a collection of my free and paid websites and Android app that offer high-quality AI-powered stem separation (aka music demixing) that run privately and offline on your devices:
* Web site: <https://freemusicdemixer.com>
* Android app: <https://freemusicdemixer.com/android>

Video showing how I use the app to practice metal (Monuments):
<iframe width="560" height="315" src="https://www.youtube.com/embed/uDUq8kOljKk?si=jYyfUDgqfh0FdPqP" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Samples of the high quality stems of the Pro Deluxe model when applied to a Periphery song.

Bass:
{% include embed-audio.html src="assets/audio/bass_pro.ogg" %}

Drums:
{% include embed-audio.html src="assets/audio/drums_pro.ogg" %}

Vocals:
{% include embed-audio.html src="assets/audio/vocals_pro.ogg" %}
<div style="height:20px;font-size:1px;">&nbsp;</div>

## Fake AI metal artist

In 2020, I created 1000sharks.xyz ([site](https://1000sharks.xyz), [repo](https://github.com/sevagh/1000sharks.xyz)), a fake metal band trained on Animals as Leaders and Cannibal Corpse:
<iframe width="777px" height="300px" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/playlists/1158301087&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/user-167126026" title="sevagh" target="_blank" style="color: #cccccc; text-decoration: none;">sevagh</a> · <a href="https://soundcloud.com/user-167126026/sets/1000sharks-ai-generated-metal" title="1000sharks - AI-generated metal" target="_blank" style="color: #cccccc; text-decoration: none;">1000sharks - AI-generated metal</a></div>
<div style="height:20px;font-size:1px;">&nbsp;</div>

## Other source separation and percussion enhancement

While not directly related to metal, groove, or rhythm, isolating the percussion in a song can be a key step in performing further percussion analysis. Besides my "Music Demixer" product, here's a list of other related projects:
* Transient shaper/percussion enhancement: [multiband-transient-shaper](https://github.com/sevagh/multiband-transient-shaper)
* Realtime harmonic-percussive source separation: [Real-Time-HPSS](https://github.com/sevagh/Real-Time-HPSS), [Zen](https://github.com/sevagh/Zen)
* Analysis of simple and complex source separation algorithms from the angle of time-frequency: [Music-Separation-TF](https://github.com/sevagh/Music-Separation-TF)
* Custom source separation AI models: [MiXiN](https://github.com/sevagh/MiXiN), [xumx-sliCQ](https://github.com/sevagh/xumx-sliCQ)
* Custom C++ inference for PyTorch source separation models: [umx.cpp](https://github.com/sevagh/umx.cpp), [demucs.cpp](https://github.com/sevagh/demucs.cpp)

