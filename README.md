# Varro Voice Server

**Status:** Planned  
**Technologies:** Python · Speech-to-Text · Text-to-Speech · VAD · Audio Streaming

## Overview

Varro Voice Server is a speech-processing service that connects Varro's audio interfaces to its orchestrator. I am designing it to handle low-latency transcription, spoken responses, and voice-session management separately from the language-model inference backend.

The **Varro** name honors Marcus Terentius Varro, a Roman scholar recognized for organizing knowledge across many disciplines.

## Key Design Choices

- **Shared speech pipeline:** Accept audio from the networked Voice Station or through Varro Mobile on behalf of the Bluetooth Companion.
- **Streaming processing:** Coordinate voice activity detection, speech-to-text, and text-to-speech with an emphasis on responsiveness.
- **Orchestrator boundary:** Forward recognized text and session identity to the orchestrator, then synthesize its response for playback.
- **Optional speaker verification:** Allow server-side voice checks and rejection handling without making them a prerequisite for basic operation.
- **Model flexibility:** Evaluate speech engines independently; no final STT or TTS model has been selected.

## Roadmap

- [ ] Define audio formats, transport, and session APIs.
- [ ] Implement a basic streaming transcription path.
- [ ] Connect transcripts and responses to the Varro Orchestrator.
- [ ] Add speech synthesis and optional speaker verification.
- [ ] Test interruption handling, latency, and multiple concurrent sessions.

## Usage

### Requirements

### Setup

### Configuration

### Operation
