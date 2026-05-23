# Project Overview: Bark TTS

This project is a Python-based implementation of **Suno AI's Bark**, a transformer-based text-to-audio model. Bark can generate highly realistic, multilingual speech as well as other audio, including music, background noise, and simple sound effects.

## Technologies
- **Language:** Python >= 3.11
- **Core Library:** `suno-bark` (sourced from GitHub)
- **Dependency Management:** `uv`
- **Audio Processing:** `scipy` for saving WAV files, `IPython` for notebook playback.

## Project Structure
- `main.py`: Entry point for generating audio from text prompts.
- `pyproject.toml`: Project configuration and dependencies.
- `uv.lock`: Locked dependency versions.

---

## Building and Running

### Prerequisites
Ensure you have `uv` installed.

### Setup
Install dependencies using `uv`:
```bash
uv sync
```

### Running the Project
Execute the main script to generate audio:
```bash
uv run main.py
```
This will download the necessary models (on first run), generate audio from a hardcoded prompt, and save it to `output.wav`.

### Testing
There are currently no automated tests. 
- TODO: Implement unit tests for audio generation utilities.

---

## Development Conventions

- **Environment:** Use `uv` for all package management and execution to ensure consistency.
- **Model Management:** Models are preloaded using `preload_models()`. Be aware that these are large and will be cached locally.
- **Code Style:** Follow standard PEP 8 guidelines for Python code.
- **Audio Output:** Default output format is WAV at the `SAMPLE_RATE` provided by the `bark` library.
