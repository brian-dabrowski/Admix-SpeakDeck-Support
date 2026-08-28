# Admix SpeakDeck Privacy Policy

**Effective date:** August 28, 2026

Admix SpeakDeck is a local Windows plugin for Elgato Stream Deck. Admix
SpeakDeck itself does not create an account, display advertising, run analytics,
or transmit selected text, microphone audio, transcripts, settings, or
diagnostic logs to Admix or any remote service.

## Data the plugin processes

Admix SpeakDeck processes the following data only to perform actions requested
by the user:

- **Selected text:** A tap sends the standard Windows Ctrl+C shortcut and reads
  the resulting clipboard text into memory for speech playback. The selection
  therefore becomes the current Windows clipboard content. Admix SpeakDeck does
  not save the text to its own files or logs.
- **Microphone audio:** While the Stream Deck key is held in dictation mode, the
  plugin captures audio from the current Windows default recording device. The
  audio is processed in memory by the bundled local speech-recognition model and
  discarded after transcription. It is not written to disk or transmitted.
- **Transcript text:** The local transcript is kept in memory only long enough
  to type it into the foreground app. Transcript content is not saved or logged.
- **Settings:** Voice, speech-rate, and gesture-timing settings are stored
  locally by the Stream Deck app as part of the user's action configuration.
- **Diagnostics:** Local rotating logs may contain timestamps, plugin state,
  selected voice name, audio-device name, character counts, durations, runtime
  details, and error messages. They do not contain selected text, content-derived
  hashes, microphone audio, or transcript text. Logs remain on the computer and
  are limited to the current log plus three archives.

## Network access and third-party voices

The Admix SpeakDeck executable does not make network requests during normal use.
Its speech-recognition model and required runtimes are bundled with the plugin.

Text-to-speech playback is performed by the Windows SAPI voice selected by the
user. Some third-party SAPI voices may independently use network services. Their
behavior, terms, and privacy practices are controlled by their publishers, not
by Admix SpeakDeck.

## Sharing and sale of data

Admix does not receive the data described above and therefore does not sell,
rent, or share it. Local data may still be available to Windows, the Stream Deck
app, the foreground app that receives dictated text, the Windows clipboard, or
an installed SAPI voice as required by those components' normal operation.

## Data removal

Removing the plugin through Stream Deck removes its installed files. A user may
also delete the local diagnostics logs without affecting saved Stream Deck
profiles. Clipboard history, Stream Deck profile settings, and text entered into
other apps are controlled by Windows, Stream Deck, and those apps respectively.

## Contact

Questions or privacy concerns can be reported through the public support page:

https://github.com/brian-dabrowski/Admix-SpeakDeck-Support

Do not include private selected text, dictated text, or other sensitive content
in a public support issue.
