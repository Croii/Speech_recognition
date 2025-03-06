# Audio Spectrogram Analysis

This project processes audio files and generates spectrograms using Python.

## Features
- Extracts spectrograms from WAV files
- Visualizes spectrograms using `matplotlib`
- Uses `scipy` for signal processing
- Includes evaluation metrics from `sklearn`

## Installation
Ensure you have the required dependencies:
```sh
pip install scipy matplotlib scikit-learn unrar
```

## Usage
1. Extract audio recordings:
   ```sh
   unrar x recordings.rar
   ```
2. Run the script to process and visualize spectrograms.

## Example
```python
from scipy.io import wavfile
from scipy import signal
import matplotlib.pyplot as plt

sample_rate, samples = wavfile.read("audio.wav")
frequencies, times, spectrogram = signal.spectrogram(samples, sample_rate)

plt.pcolormesh(times, frequencies, spectrogram)
plt.ylabel('Frequency [Hz]')
plt.xlabel('Time [sec]')
plt.show()
```

## License
MIT

