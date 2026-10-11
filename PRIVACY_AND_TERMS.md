# Privacy & Terms

DOTE Whisper is a free desktop app that transcribes recordings stored on your own computer. There are no accounts and no servers that receive your audio, so this page is short.

_Last updated 11 October 2026._ The same text is on the website at <https://dote-whisper.alexstein.ca/legal/>.

-   [Privacy Policy](#privacy-policy)
    -   [What is stored](#what-is-stored)
    -   [Your recordings](#your-recordings)
    -   [When the app goes online](#when-the-app-goes-online)
    -   [Feedback](#feedback)
    -   [The website](#the-website)
-   [Terms & Conditions](#terms--conditions)
    -   [License to use](#license-to-use)
    -   [Your responsibilities](#your-responsibilities)
    -   [No warranty](#no-warranty)
    -   [Limitation of liability](#limitation-of-liability)
-   [Contact](#contact)

## Privacy Policy

DOTE Whisper runs entirely on your computer. It decodes, transcribes and labels your recordings locally and never uploads them.

> **The short version.** We don't collect your recordings, your transcripts, your file names, or anything about how you use the app. There are no analytics, no tracking and no accounts. The app only goes online to download the models you choose, to check whether a newer version exists and, if you ask it to, to send us feedback.

### What is stored

Nothing about _you_, unless you send us feedback. Everything the app keeps is on your own computer.

| Data                                                                    | Where it lives                                                                                                                                               |
| ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Transcripts (JSON, SRT and WebVTT files)                                | Beside the original recording when _Auto-save next to source_ is on, otherwise wherever you save them.                                                       |
| Preferences: model, speaker settings, tuning values and window position | In the app's settings folder on your computer.                                                                                                               |
| Downloaded models                                                       | In the models folder shown in Settings. By default that is inside the app's settings folder.                                                                 |
| A diagnostic log of errors, warnings and update checks                  | In the app's log folder. It does not contain transcript text.                                                                                                |
| Temporary working copies of the audio                                   | In your system's temporary folder while a transcription runs. They are deleted afterwards, and any left by a crash are cleared the next time the app starts. |
| Feedback and error reports you send, from the app or the website        | A private issue on GitHub that only the developer can read. See [Feedback](#feedback).                                                                       |

### Your recordings

The app decodes your recordings with a copy of ffmpeg that ships inside it, then runs speech recognition (whisper.cpp) and speaker separation (sherpa-onnx) on your computer. It only ever reads your original files and never changes them. Nothing about their contents is sent to us or to anyone else.

### When the app goes online

| When                                                                                                                                                     | What happens                                                                                                                                                                                                                                                                                                                                                                              |
| -------------------------------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| When the app starts, and when you choose _File → Check for updates…_                                                                                     | The app asks two places at once for the latest version number and its release notes: the DOTE update server at Aalborg University (license.dote.aau.dk), and GitHub (api.github.com), for the newest release in this repository. If a newer version exists, the app tells you. It never downloads or installs anything by itself. Without an internet connection the check fails quietly. |
| The first time you use a speech-recognition model                                                                                                        | The model downloads from HuggingFace (huggingface.co). The app shows its size and asks first.                                                                                                                                                                                                                                                                                             |
| The first time you turn on speaker labels, or pick a different speaker model                                                                             | The speaker models download from HuggingFace and from the sherpa-onnx project's releases on GitHub.                                                                                                                                                                                                                                                                                       |
| When you add a custom model                                                                                                                              | The app asks HuggingFace which files the model you named contains, then downloads them. _Browse on HuggingFace_ opens the HuggingFace website in your web browser.                                                                                                                                                                                                                        |
| When you send feedback, from _Help → Send Feedback…_, the _Report…_ link beside a failed transcription, or the report offered after something goes wrong | The app sends the report to our feedback service (dote-whisper.alexstein.ca). Nothing is sent until you click _Send_, and the dialog lets you see everything that goes with your text first. See [Feedback](#feedback).                                                                                                                                                                   |

These requests carry what any web request does, such as your IP address. The privacy policies of Aalborg University, HuggingFace and GitHub apply to them. DOTE Whisper does not sell data, show ads, or share information with advertisers.

### Feedback

A report holds what you write, the type you choose, and your email address if you give one. From the app it also holds the app version, your operating system and its version, your computer's processor, memory and graphics, and the settings of your last transcription: the model, the languages you chose and the speaker settings. After an error it holds the error message and stack trace too, unless you untick that. If you tick _Include the app's recent log_, it also holds the end of the app's diagnostic log, which can name your recordings' files. The name of your home folder is removed from both. From the website, a bug report holds the app version and operating system you enter, and your browser's identification.

Reports never include your recordings or transcripts, and name your files only where an error message, or the log you chose to include, does. Our feedback service files each one as a private issue on GitHub that only the developer can read, and uses your email address only to reply to it. The service sees your IP address, as every web request does, and keeps it in memory for a day at most, only to limit how many reports can be sent from one place.

### The website

The website (<https://dote-whisper.alexstein.ca>) has no analytics or cookies. It loads fonts from Google Fonts, and the download page asks GitHub which installer files are available so its buttons can link straight to them. The [Feedback](https://dote-whisper.alexstein.ca/feedback/) page sends what you enter to our feedback service, as described above. Your light or dark theme choice is saved in your own browser and nowhere else.

## Terms & Conditions

By downloading and using DOTE Whisper, you agree to these terms. We've tried to keep them fair and readable, so please do read them.

### License to use

DOTE Whisper is free to use under the [DOTE Whisper Freeware License](LICENSE.md), for personal, academic, commercial and institutional use, on as many computers as you like. You may also share the unmodified installers, free of charge. The app's source code is not published. The open-source parts it is built on keep their own licenses: whisper.cpp (MIT), sherpa-onnx (Apache 2.0) and ffmpeg (LGPL/GPL). Each model you download also keeps its own license. The standard Whisper models are MIT-licensed; community models from HuggingFace vary, so check the model's page before you rely on it.

### Your responsibilities

1. **Check your transcripts.** Automatic transcripts and speaker labels contain mistakes. You are responsible for reviewing them before you quote, publish or otherwise rely on them.
2. **Keep your originals.** The app never modifies source recordings. Keep them, since the recording, not the transcript, is the primary record.
3. **Use recordings you're entitled to.** You're responsible for having the right to process the recordings you use, and for following any consent, ethics or data-handling rules that apply to them and to the transcripts you make.
4. **Use the software lawfully.** Don't use DOTE Whisper for anything unlawful, including recording or transcribing people without the consent the law requires.

### No warranty

The software is provided **"as is"**, without warranty of any kind, express or implied, including but not limited to the warranties of merchantability, fitness for a particular purpose, and non-infringement. We do not guarantee that the software will be uninterrupted or error-free, or that any transcript or speaker label will be correct.

### Limitation of liability

To the fullest extent permitted by law, the authors and contributors of DOTE Whisper shall not be liable for any data loss or for any direct, indirect, incidental, special, or consequential damages arising out of the use of, or inability to use, the software, even if advised of the possibility of such damages.

> We may update these terms and this policy as the app evolves. When we do, we'll change the "last updated" date above. Continued use after a change means you accept the revised version.

## Contact

Questions about privacy or these terms? Use the [feedback page](https://dote-whisper.alexstein.ca/feedback/), or [open an issue](https://github.com/LiminalSpaces/dote-whisper-dist/issues) on this repository.
