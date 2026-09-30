# youtube-chapter-marker-builder

Validate and format YouTube chapter timestamps. Two input modes (row-by-row or paste-block). Browser only.

An independent project. Not affiliated with, endorsed by, or sponsored by YouTube or Google LLC.

**Live demo:** https://0xelitesystem.github.io/youtube-chapter-marker-builder/

## Use

Open [`index.html`](./index.html). Choose row-by-row or paste mode. Enter your chapters. Click Validate. Copy the formatted output into your video description.

The tool checks against YouTube's chapter rules:

- First chapter must be at `0:00`
- At least 3 chapters total
- Each chapter must be at least 10 seconds long
- Timestamps must be ascending
- Format `MM:SS` or `H:MM:SS`

If any check fails, YouTube won't render the chapter UI on your video. The tool tells you exactly what's wrong before you publish.

## Why

The chapter markers in your description are silently picky. If even one rule is broken (timestamp not at 0:00, gap under 10 seconds, format off by a colon), YouTube falls back to no chapters and gives no error message. You only find out by watching your published video.

This tool catches all of that in advance.

## Privacy

All validation runs in your browser. No requests, no analytics, no third-party scripts.

## Run locally

```
git clone https://github.com/0xelitesystem/youtube-chapter-marker-builder
cd youtube-chapter-marker-builder
```

Open `index.html` in any browser. Or:

```
python -m http.server 8000
```

## Contribute

PRs welcome:

- Import from a transcript or SRT file (auto-detect chapter breaks)
- Validate against the chapter title length limit
- Detect duplicate or near-duplicate titles
- Localized chapter name conventions

Don't add: external scripts, npm dependencies, telemetry. Single file by design.

## Build

No build. Single HTML file.

## More

Part of a catalog of single-file browser tools and plain-language references, all MIT licensed and dependency-free: [0xelitesystem.github.io](https://0xelitesystem.github.io/). Built by [elitesystem.ai](https://elitesystem.ai).

## License

MIT.

## Related

- [youtube-thumbnail-tester](https://github.com/0xelitesystem/youtube-thumbnail-tester) - thumbnail placement preview
- [youtube-title-ab-tester](https://github.com/0xelitesystem/youtube-title-ab-tester) - title comparison
- [video-srt-cleaner](https://github.com/0xelitesystem/video-srt-cleaner) - clean auto-generated captions
- [video-description-templates](https://github.com/0xelitesystem/video-description-templates) - description box templates
