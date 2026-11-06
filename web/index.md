---
keywords: metal, groove, beats, beat tracking, tempo, beat, drums, percussion, percussive, headbang, rhythm, metronome, polyrhythm, multimeter
description: "Beat tracking, tempo estimation, percussive source separation, and other music analysis tools for rhythm in metal music."
---

I'm Sevag and I love metal. This page is an homage to how that love turned into a pile of projects on groove and rhythm in metal music, and eventually into Music Demixer, my best project yet. See my [open-source portfolio](https://github.com/sevagh) and my [personal website](https://sevag.xyz) for any inquiries.
<br style="line-height:0px;" />

## Music Demixer: practice tools for metal

[Music Demixer](https://musicdemixer.com) is my online tool for musicians, and the project that grew most directly out of playing metal. These are the parts I use to learn and practice:

* [Click Track](https://musicdemixer.com/click-track): a click that follows the drummer's own timing, with the song split into stems. Mute the drums and play along with the click and the band, and take the tempo map into your DAW as MIDI.
* [Drum separation](https://musicdemixer.com/drums): pull the drums out of a song, or split the kit into kick, snare, toms and cymbals to hear exactly what the drummer is playing.
* [Drum MIDI](https://musicdemixer.com/drums): transcribe the drum part to MIDI and load it into your DAW or drum software.
* [Guitar Tab](https://musicdemixer.com/guitar-tab) (beta): turn a riff into an editable Guitar Pro tab, in standard or drop tunings down to Drop C.
* [Stem separation](https://musicdemixer.com/stem-separation): isolate the bass, guitar, vocals or drums to learn a part, or make your own backing track.

You can preview one song for free.

Drum MIDI transcribed from a djent drum track, played back through a drum sampler:
{% include embed-video.html src="https://musicdemixer.com/assets/clips/drum-stems/djent-vibe-drums-visualizer.mp4" type="video/mp4" %}

The same kit split into pieces. Kick:
{% include embed-audio.html src="https://musicdemixer.com/assets/clips/drum-stems/djent-vibe-kick.mp3" type="audio/mpeg" %}

Snare:
{% include embed-audio.html src="https://musicdemixer.com/assets/clips/drum-stems/djent-vibe-snare.mp3" type="audio/mpeg" %}

Cymbals:
{% include embed-audio.html src="https://musicdemixer.com/assets/clips/drum-stems/djent-vibe-cymbals.mp3" type="audio/mpeg" %}

A guitar tab transcribed from a recording, played back:
{% include embed-video.html src="https://musicdemixer.com/assets/clips/guitar-tab/guitar-tab-playback.mp4" type="video/mp4" %}
<div style="height:20px;font-size:1px;">&nbsp;</div>

## If you're still curious

Before Music Demixer, the same obsession produced these open-source projects and experiments.
<div style="height:20px;font-size:1px;">&nbsp;</div>

### Rhythm and beats

#### Motion and percussion-aligned beat tracking

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

#### Polyrhythmic metronome and a drum machine

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

#### Beat-driven visual animation on Android

ElectroPARTYogram: [repo](https://github.com/sevagh/ElectroPARTYogram)

Tempo and beat-driven animation in an Android app, powered by [BTrack](https://github.com/adamstark/BTrack) and animated with [SFML](https://www.sfml-dev.org/), with visualization intensity influenced by onset strength:
{% include embed-video.html src="assets/video/animals_as_leaders_the_woven_web.webm" %}
<div style="height:20px;font-size:1px;">&nbsp;</div>

### Drums and percussion

Isolating the percussion in a song can be a key step in performing further percussion analysis.

* Transient shaper/percussion enhancement: [multiband-transient-shaper](https://github.com/sevagh/multiband-transient-shaper)
* Realtime harmonic-percussive source separation: [Real-Time-HPSS](https://github.com/sevagh/Real-Time-HPSS), [Zen](https://github.com/sevagh/Zen)

<div style="height:20px;font-size:1px;">&nbsp;</div>

### Separating metal songs

* Custom source separation AI models: [MiXiN](https://github.com/sevagh/MiXiN), [xumx-sliCQ](https://github.com/sevagh/xumx-sliCQ)
* Analysis of simple and complex source separation algorithms from the angle of time-frequency: [Music-Separation-TF](https://github.com/sevagh/Music-Separation-TF)
* A stem dataset for music demixing research: [OnAir-Music-Dataset](https://github.com/sevagh/OnAir-Music-Dataset), with the [onair-py](https://github.com/sevagh/onair-py) loader

<div style="height:20px;font-size:1px;">&nbsp;</div>

### Running it fast

* Custom C++ inference for PyTorch source separation models: [umx.cpp](https://github.com/sevagh/umx.cpp), [demucs.cpp](https://github.com/sevagh/demucs.cpp), [demucs.onnx](https://github.com/sevagh/demucs.onnx)

<div style="height:20px;font-size:1px;">&nbsp;</div>

### Just for fun: a fake AI metal artist

In 2020, I created 1000sharks.xyz ([site](https://1000sharks.xyz), [repo](https://github.com/sevagh/1000sharks.xyz)), a fake metal band trained on Animals as Leaders and Cannibal Corpse:
<iframe width="777px" height="300px" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/playlists/1158301087&color=%23ff5500&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true&visual=true"></iframe><div style="font-size: 10px; color: #cccccc;line-break: anywhere;word-break: normal;overflow: hidden;white-space: nowrap;text-overflow: ellipsis; font-family: Interstate,Lucida Grande,Lucida Sans Unicode,Lucida Sans,Garuda,Verdana,Tahoma,sans-serif;font-weight: 100;"><a href="https://soundcloud.com/user-167126026" title="sevagh" target="_blank" style="color: #cccccc; text-decoration: none;">sevagh</a> · <a href="https://soundcloud.com/user-167126026/sets/1000sharks-ai-generated-metal" title="1000sharks - AI-generated metal" target="_blank" style="color: #cccccc; text-decoration: none;">1000sharks - AI-generated metal</a></div>
<div style="height:20px;font-size:1px;">&nbsp;</div>
