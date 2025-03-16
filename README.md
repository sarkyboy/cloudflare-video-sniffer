# Cloudflare Video Sniffer

A Cloudflare Worker service that extracts video links from web pages. This tool helps you find direct video URLs from various web pages by analyzing video tags, source tags, and common video player configurations.

## Features

- Extracts video links from HTML5 video tags
- Supports various video formats (MP4, WebM, OGG, MOV, M3U8)
- Handles both relative and absolute URLs
- Detects video links in player configurations
- CORS enabled for cross-origin requests
- Lightweight and efficient

## Usage

Send a POST request to your Cloudflare Worker endpoint with the following JSON payload:

```json
{
  "url": "https://example.com/page-with-videos"
}
```

The service will return a JSON response containing the found video links:

```json
{
  "url": "https://example.com/page-with-videos",
  "videos": [
    "https://example.com/video1.mp4",
    "https://example.com/video2.webm"
  ]
}
```

## Deployment

1. Create a new Cloudflare Worker
2. Copy the code into your Worker
3. Deploy and use your Worker's URL as the endpoint

## License

MIT License

## Author

sarkyboy