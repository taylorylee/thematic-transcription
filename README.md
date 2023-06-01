# Thematic Transcription

A tool to transcribe video to audio using Whisper API for thematic analysis. 

Attention weights to capture dependencies and interactions between words in the audio.

The following is split up into a few sections:
(1) Focused on transcription and performing speaker diarization, meaning separating speakers in the audio
(2) Thematic analysis of the transcription (in progress)

## Installation

1. Set up  Whisper API [GitHub instructions](https://github.com/openai/whisper)

If you do not have admin access, make sure to `run as administrator` when installing

2. Install dependencies in your command prompt

`pip install whisper`
`pip install python-docx`
`pip install fpdf`

3. Add audio file to the same directory or add the correct path in code

4. Modify code as necessary such as changing the name of the audio file, language, etc.

5. Run the script. Replace `your_script.py` with the name of your script

`python your_script.py`

6. See saved transcription as a word (.docx) and pdf (.pdf) file in the same directory as the audio file

## Acceptable file types

The acceptable file types[^1] are:

- `m4a`: MPEG-4 Audio File
- `mp3`: MPEG-1 Audio Layer 3 File
- `webm`: WebM Audio/Video File
- `mp4`: MPEG-4 Video File
- `mpga`: MPEG Audio File
- `wav`: Waveform Audio File
- `mpeg`: MPEG Movie File

Links to audio files are not supported at the moment.

## Requests per minute

50 requests per minute[^1]

## File size

Up to 25MB[^1]

## Command prompts

### Transcribe audio

1. `cd` into the directory where the audio file is located
2. `whisper transcribe --filename <filename> --language <language> --output <output_filename>`
    - `filename` is the name of the file you want to transcribe
    - `language` is the language of the audio file
    - `output` is the name of the file you want to save the transcription as

### Transcribe audio with speaker separation

1. `cd` into the directory where the audio file is located
2. `whisper transcribe --filename <filename> --language <language> --output <output_filename> --speaker-separation`
    - `filename` is the name of the file you want to transcribe
    - `language` is the language of the audio file
    - `output` is the name of the file you want to save the transcription as

### Transcribe audio with speaker separation and speaker labels

1. `cd` into the directory where the audio file is located
2. `whisper transcribe --filename <filename> --language <language> --output <output_filename> --speaker-separation --speaker-labels`
    - `filename` is the name of the file you want to transcribe
    - `language` is the language of the audio file
    - `output` is the name of the file you want to save the transcription as

### Transcribe audio with speaker separation and speaker labels and punctuation

1. `cd` into the directory where the audio file is located
2. `whisper transcribe --filename <filename> --language <language> --output <output_filename> --speaker-separation --speaker-labels --punctuation`
    - `filename` is the name of the file you want to transcribe
    - `language` is the language of the audio file
    - `output` is the name of the file you want to save the transcription as

### Transcribe audio with speaker separation and speaker labels and punctuation and profanity filter

1. `cd` into the directory where the audio file is located
2. `whisper transcribe --filename <filename> --language <language> --output <output_filename> --speaker-separation --speaker-labels --punctuation --profanity-filter`
    - `filename` is the name of the file you want to transcribe

[^1]: [Whisper API FAQ](https://help.openai.com/en/articles/7031512-whisper-api-faq)

## License

[MIT](LICENSE)
