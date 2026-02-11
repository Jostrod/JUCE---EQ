# JUCE--EQ

⚠️ Status: Still in early development, work in progress


## Overview

A real-time three-band audio equalizer built in C++ using the JUCE framework.

The goal of this project is to deepen understanding of:
- Digital signal processing (DSP)
- IIR filter design
- Real-time audio constraints
- Plugin architecture (VST3 / AU)

The EQ consists of:
- Low band (shelving filter)
- Mid band (peak filter)
- High band (shelving filter)

---

## Technical Focus

This project emphasizes:

- Real-time safe processing (no heap allocation in audio thread)
- Parameter smoothing
- Filter coefficient recalculation
- Separation between GUI and DSP layer
- Clean architecture and maintainability

---

## Current Features

- [x] JUCE project setup
- [x] AudioProcessor / AudioProcessorEditor structure
- [x] Basic three-band filtering
- [x] Gain control per band
- [ ] Q control for mid band
- [ ] Frequency control per band
- [ ] Parameter smoothing
- [ ] Bypass per band
- [ ] Visual frequency response graph

---

## DSP Implementation

Filters are implemented using:

- IIR filters (biquad topology)
- Coefficient calculation via JUCE DSP module
- Real-time parameter updates

Future improvements include:
- Manual coefficient implementation
- Oversampling
- Denormal number protection
- SIMD optimization

---

## Build Instructions

1. Install JUCE
2. Open project in Projucer
3. Generate project files
4. Build using Visual Studio / Xcode

---

## Architecture

- `PluginProcessor` – DSP logic
- `PluginEditor` – GUI layer
- Parameter management via AudioProcessorValueTreeState

The project is structured to keep DSP logic independent from UI logic.

---

## Why This Project?

This project is part of a broader focus on:

- Performance-oriented C++
- Systems-level programming
- Audio and signal processing
- Real-time software engineering

The long-term goal is to build production-level audio tools while
maintaining strict real-time safety constraints.

---

## Roadmap

- Implement full parameter control
- Add response curve visualization
- Add preset system
- Benchmark CPU usage
- Refactor into reusable DSP modules

---
