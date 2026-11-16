# MakeItScroll

A lightweight, mobile-friendly teleprompter with built-in video recording. Write your script, adjust your reading pace, and record a take—all from your browser.

**[Open MakeItScroll →](https://hammel-c.github.io/MakeItScroll/)**

Built with HTML, CSS, and JavaScript in a single `index.html` file. No installation, account, build process, or backend required.

## Features

### Teleprompter

- Adjustable text size and scrolling speed.
- Play, pause, restart, and manually reposition your script.
- Mirror text for use with a physical teleprompter.
- Word count, character count, and estimated scrolling time.
- Text editor that grows with your script.
- Clipboard paste, clear text, and restore-default actions.
- Fullscreen support, with an expanded-view fallback where native fullscreen is unavailable.
- Script and preference storage in your browser, when local storage is available.

### Camera and audio

- Record video while reading your script.
- Test your camera and microphone before recording.
- Check microphone activity with a live audio-level meter.
- Switch between front and rear cameras.
- Select available camera and microphone inputs.
- Record with or without microphone audio.
- Choose a top/bottom or left/right split and resize it by dragging the divider.
- Position teleprompter and camera controls independently.
- See a red border around the camera preview while recording.

### Recorded takes

- Review recordings in the takes modal.
- View each take’s duration, file size, resolution, and audio status.
- Download individual videos or all takes in one ZIP file.
- Share videos through the device’s native share sheet where supported.
- On compatible iPhones and iPads, choose **Save Video** from the share sheet to add a take to Photos.
- Delete all takes from the current tab with confirmation.

## Getting started

1. Open **[MakeItScroll](https://hammel-c.github.io/MakeItScroll/)**.
2. Write or paste your script.
3. Open **Teleprompter Controls** and adjust the font size, speed, and control positions.
4. To record, enable **camera & video recording**, select your layout and inputs, and test your devices.
5. Press **↖ Make-It-Scroll ↘** to enter scrolling mode.

### Camera controls

| Control | Action |
| --- | --- |
| 🔴 | Start or stop recording |
| 🔄 | Switch between front and rear cameras |
| 📸 | Turn the camera on or off |
| 🎬 | Open recorded takes; the badge shows the current take count |

Pausing the teleprompter pauses **only the text**. Use 🔴 to stop recording.

> [!IMPORTANT]
> Recorded takes are held temporarily in the current tab’s memory. Download or save them before closing or reloading the page. Saving your script does not save your recordings.

## Running locally

Download the repository or save [`index.html`](index.html) to your device.

For text-only use, open the file in a modern browser. For reliable camera and microphone access, serve it through **HTTPS or localhost**.

If Python is installed, run this command from the folder containing `index.html`:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

> [!NOTE]
> Opening a computer’s ordinary HTTP address from a phone—for example, `http://192.168.1.10:8000`—does not provide the same camera-access exception as localhost. Use an HTTPS address when testing from another device.

## Browser support

Chromium-based browsers are the primary tested environment.

Camera recording, input selection, fullscreen, file sharing, and saving to Photos depend on the browser, operating system, and connected devices. Some mobile browsers expose fewer input choices or provide an expanded view instead of native fullscreen.

Videos are exported as **MP4 or WebM**, depending on the formats supported by the browser. The scrolling-time display is an estimate based on the current script, font size, layout, and speed.

## Privacy

MakeItScroll processes scripts, camera previews, and recordings in your browser. The application does not upload your scripts or recordings to a server.

Scripts and preferences may be stored locally in your browser. Recorded takes remain in memory until you download them, delete them, or leave the page.

## Contributing

Bug reports and improvements are welcome.

When reporting a problem, include:

- Your device, operating system, and browser version.
- Steps to reproduce the issue.
- Any warning or error displayed by the application.
- Whether you are using the hosted site or a local copy.

## Acknowledgements

Developed with AI-assisted coding tools, including v0 by Vercel, Gemini 3.0 Pro, and ChatGPT/Codex.

## License

Licensed under the **GNU General Public License v3.0**.
