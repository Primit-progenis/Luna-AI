# Luna AI

Luna is an early Python voice-assistant experiment. It listens through a microphone, converts speech to text, matches a few phrases, and responds using text-to-speech.

## How it works

1. At startup, Luna gives a time-based greeting.
2. It captures one spoken request with the microphone and uses Google's speech-recognition service with the `en-in` locale.
3. A series of phrase checks selects an action. Current examples include reading a short Wikipedia summary, telling the time, opening websites, and speaking fixed responses.
4. The `speak()` helper reads responses aloud through `pyttsx3`.

The location, music suggestions, jokes, and email recipient are fixed examples in the code. They are not live location, recommendation, or contact integrations.

## Requirements

The script imports:

- `pyttsx3` for speech output
- `SpeechRecognition` and a working microphone/audio backend for speech input
- `wikipedia` for summaries

It also uses Python's standard `datetime`, `smtplib`, `webbrowser`, and `os` modules. Install the third-party packages in your Python environment, then run:

```sh
python luna.ai
```

A microphone is required for voice input. Speech recognition uses an online service, and opening websites requires a browser.

## Current limitations

The email helper is not configured for use: it contains placeholder account values and a nonstandard SMTP port. The VS Code action contains a machine-specific Windows path. Do not add real passwords or other credentials directly to the script.
