# Soundness CLI

## Overview
Soundness CLI is a command-line interface tool designed for audio analysis and sound processing. This tool provides developers and audio engineers with powerful capabilities to analyze, process, and manipulate audio files from the command line.

## Features
- **Audio Analysis**: Comprehensive audio file analysis including frequency spectrum, amplitude, and waveform analysis
- **Format Support**: Support for multiple audio formats (WAV, MP3, FLAC, OGG, etc.)
- **Batch Processing**: Process multiple audio files simultaneously
- **Real-time Processing**: Real-time audio stream analysis
- **Export Options**: Export analysis results in various formats (JSON, CSV, XML)
- **Cross-platform**: Works on Windows, macOS, and Linux

## Installation

### Prerequisites
- Node.js (v16 or higher)
- npm or yarn package manager
- FFmpeg (for advanced audio processing)

### Install from npm
```bash
npm install -g soundness-cli
```

### Install from source
```bash
git clone https://github.com/wearedood/Soundness_cli.git
cd Soundness_cli
npm install
npm run build
npm link
```

## Usage

### Basic Commands

#### Analyze an audio file
```bash
soundness analyze input.wav
```

#### Batch process multiple files
```bash
soundness batch-analyze *.wav --output results/
```

#### Real-time audio analysis
```bash
soundness live --input microphone
```

### Advanced Options

#### Specify output format
```bash
soundness analyze input.wav --format json --output analysis.json
```

#### Custom analysis parameters
```bash
soundness analyze input.wav --fft-size 2048 --window hamming
```

## Configuration

Create a `.soundnessrc` file in your project root:

```json
{
  "defaultFormat": "json",
  "outputDirectory": "./analysis",
  "fftSize": 1024,
  "windowFunction": "hann",
  "sampleRate": 44100
}
```

## API Reference

### Commands

| Command | Description | Options |
|---------|-------------|---------|
| `analyze` | Analyze a single audio file | `--format`, `--output`, `--fft-size` |
| `batch-analyze` | Analyze multiple audio files | `--output`, `--parallel` |
| `live` | Real-time audio analysis | `--input`, `--buffer-size` |
| `convert` | Convert between audio formats | `--format`, `--quality` |
| `help` | Show help information | N/A |

### Output Formats

- **JSON**: Structured data format for programmatic use
- **CSV**: Spreadsheet-compatible format
- **XML**: Markup format for data exchange
- **TXT**: Human-readable text format

## Examples

### Example 1: Basic Audio Analysis
```bash
# Analyze a WAV file and output JSON
soundness analyze song.wav --format json
```

### Example 2: Batch Processing
```bash
# Process all MP3 files in a directory
soundness batch-analyze music/*.mp3 --output analysis/ --parallel 4
```

### Example 3: Real-time Monitoring
```bash
# Monitor microphone input in real-time
soundness live --input microphone --buffer-size 1024
```

## Contributing

We welcome contributions! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Setup

```bash
git clone https://github.com/wearedood/Soundness_cli.git
cd Soundness_cli
npm install
npm run dev
```

### Running Tests

```bash
npm test
npm run test:coverage
```

## Troubleshooting

### Common Issues

**Issue**: "FFmpeg not found"
**Solution**: Install FFmpeg and ensure it's in your system PATH

**Issue**: "Permission denied"
**Solution**: Run with appropriate permissions or use `sudo` on Unix systems

**Issue**: "Unsupported audio format"
**Solution**: Convert your audio file to a supported format (WAV, MP3, FLAC)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Support

- 📧 Email: support@wearedood.com
- 🐛 Issues: [GitHub Issues](https://github.com/wearedood/Soundness_cli/issues)
- 📖 Documentation: [Wiki](https://github.com/wearedood/Soundness_cli/wiki)
- 💬 Discussions: [GitHub Discussions](https://github.com/wearedood/Soundness_cli/discussions)

## Changelog

See [CHANGELOG.md](CHANGELOG.md) for a list of changes and version history.
