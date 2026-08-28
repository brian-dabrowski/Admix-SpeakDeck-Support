# Admix SpeakDeck Support

## Requirements

- Windows 11, 64-bit
- Stream Deck 7.1 or newer
- An enabled Windows SAPI voice
- Windows desktop-app microphone access for dictation
- A current Vulkan-capable GPU driver is recommended; CPU fallback is included

No separate .NET, Python, CUDA, Vulkan SDK, Whisper, or Microsoft Visual C++
runtime installation is required.

## Controls

- **Tap:** Read the current text selection.
- **Double-tap:** Stop active speech or dictation.
- **Hold:** Wait for the key to turn blue and play the ready chime, speak, then
  release to transcribe and type into the focused app.

## Troubleshooting

### A tap does not read anything

1. Select text before pressing the key.
2. Open the action settings and use **Test Voice**.
3. Confirm that an enabled playback voice is selected.
4. Confirm the Windows default playback device can produce sound.
5. If the target app is running as administrator, launch it normally; Windows
   blocks a normal Stream Deck process from sending Ctrl+C into an elevated app.

### Hold-to-dictate does not start

1. Keep holding until the key turns blue and the ready chime plays.
2. In **Windows Settings → Privacy & security → Microphone**, enable microphone
   access and **Let desktop apps access your microphone**.
3. Confirm that the intended microphone is the Windows default recording device.

### Dictation is slow

The first hold after Stream Deck starts warms the local model. A current GPU
driver enables Vulkan acceleration on compatible hardware; otherwise the plugin
uses the CPU automatically. No Vulkan SDK or CUDA toolkit should be installed.

### Text is not inserted after transcription

Keep the original text field focused until the blue processing indicator clears.
Windows will not allow a normally launched Stream Deck to type into an
administrator-elevated app.

## Diagnostics

The local log is stored at:

```text
%APPDATA%\Elgato\StreamDeck\Plugins\com.admix.speechdeck.sdPlugin\logs\AdmixSpeechDeck.log
```

When reporting a problem, include the Windows version, Stream Deck version, GPU
model, what the key displayed, and the relevant log excerpt. The plugin does not
log selected text, microphone audio, or transcripts, but review any diagnostic
file before posting it publicly.

[Open a support issue](https://github.com/brian-dabrowski/Admix-SpeakDeck-Support/issues)
