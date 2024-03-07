# error pip install whisper_mic

**error message**   
note: This error originates from a subprocess, and is likely not a problem with pip.
ERROR: Failed building wheel for pyaudio
Failed to build pyaudio
ERROR: Could not build wheels for pyaudio, which is required to install pyproject.toml-based projects

**take care**
```bash
sudo apt update
sudo apt install python3-pip
sudo apt install portaudio19-dev python3-pyaudio python3-all-dev
```

```python
pip3 install pyaudio
```
