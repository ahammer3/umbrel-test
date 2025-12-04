# Whisper STT (ahammer3-whisper)

Local, offline speech-to-text using Faster-Whisper, packaged as an Umbrel
Community App. Once installed, it exposes an HTTP API at:

    http://umbrel.local:9001/transcribe

Example `curl`:

```bash
curl -X POST "http://umbrel.local:9001/transcribe"   -H "Content-Type: multipart/form-data"   -F "audio_file=@audio.wav"
```

Response:

```json
{ "text": "hello how are you" }
```

You can use this inside a local voice assistant pipeline together with llama-gpt
and Kokoro on Umbrel.
