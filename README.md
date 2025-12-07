# RMBG - Free AI Background Remover

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![Demo](https://img.shields.io/badge/Demo-rmbg.dev-blue)](https://rmbg.dev)

A **100% privacy-focused** AI background remover that runs entirely in your browser. No uploads, no servers, no data collection.

[English](https://rmbg.dev) | [中文](https://rmbg.dev/zh/)

## Features

- **100% Private** - Images never leave your device. All AI processing happens locally in your browser.
- **Forever Free** - No limits, no watermarks, no sign-up required.
- **Instant Processing** - WebGPU acceleration for lightning-fast results.
- **Batch Processing** - Process multiple images at once.
- **Works Offline** - Once the model is cached, works without internet.
- **State-of-the-Art AI** - Powered by [RMBG-1.4](https://huggingface.co/briaai/RMBG-1.4) deep learning model.

## How It Works

1. First visit downloads the AI model (~234MB) to browser cache
2. Model runs locally using WebGPU (GPU) or WebAssembly (CPU) fallback
3. Images are processed entirely on your device
4. Results are generated instantly without any server communication

## Tech Stack

- **AI Model**: [RMBG-1.4](https://huggingface.co/briaai/RMBG-1.4) (ONNX format)
- **Runtime**: [ONNX Runtime Web](https://onnxruntime.ai/) with WebGPU/WASM backends
- **Frontend**: Vanilla HTML/CSS/JavaScript (no framework dependencies)

## Browser Support

| Browser | WebGPU | WASM Fallback |
|---------|--------|---------------|
| Chrome 113+ | Yes | Yes |
| Edge 113+ | Yes | Yes |
| Firefox | No | Yes |
| Safari 18+ | Yes | Yes |

## Local Development

Simply serve the files with any static file server:

```bash
# Using Python
python -m http.server 8080

# Using Node.js
npx serve .

# Using PHP
php -S localhost:8080
```

Then open `http://localhost:8080` in your browser.

## Project Structure

```
rmbg/
├── index.html      # English version
└── zh/
    └── index.html  # Chinese version
```

## Privacy

This tool is designed with privacy as the #1 priority:

- **No server uploads** - Your images never leave your browser
- **No analytics on images** - We only track page views, not your content
- **No cookies for tracking** - No third-party tracking
- **Open source** - Verify the code yourself

## Credits

- AI Model: [BRIA AI - RMBG-1.4](https://huggingface.co/briaai/RMBG-1.4)
- Runtime: [ONNX Runtime](https://onnxruntime.ai/)

## License

MIT License - feel free to use, modify, and distribute.

---

Made with privacy in mind.
