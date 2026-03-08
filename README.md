# PasteDrop

A lightweight clipboard downloader built as a single-page site.

PasteDrop lets you press `Ctrl+V` (or click the paste zone) to instantly download clipboard content like images, files, and text, with a clean local history list.

## Highlights

- Single file app (`index.html`), no build tools needed
- Warm amber dark theme UI
- Supports clipboard images, files, and plain text
- Auto-download on paste
- History cards with:
  - type badge
  - size and timestamp
  - download again button
  - remove button
- Clear all history action
- Local-first behavior (no upload logic)

## Quick Start

1. Download or clone this repo.
2. Open `index.html` in a modern browser.
3. Click the paste zone or press `Ctrl+V`.
4. Your clipboard item downloads automatically.

Optional local server:

```bash
python -m http.server 5500
```

Then open `http://localhost:5500`.

## Supported Clipboard Content

| Content type | What PasteDrop does |
| --- | --- |
| Image (`image/*`) | Downloads file and shows thumbnail in history |
| File-like clipboard item | Downloads using detected MIME type |
| Plain text (`text/plain`) | Saves as a `.txt` file |

## Privacy

PasteDrop is designed to run in the browser only.

- No backend
- No database
- No upload requests in app logic

## Browser Notes

- `Ctrl+V` paste handling works broadly in modern browsers.
- Click-to-read clipboard (`navigator.clipboard.read`) may require secure context (`https` or `localhost`) and user permission.

## Project Structure

```text
.
|-- index.html
|-- README.md
```

## Customize

Most theme values are in CSS variables under `:root` inside `index.html`, including:

- background and panel colors
- accent colors
- borders and shadows
- text and muted text colors
