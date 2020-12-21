# AirPlay
Working towards a stable(ish) AirPlay 2 package to be used by services such as [shairport-sync](https://github.com/mikebrady/shairport-sync).

Information on this page could (and probably will be) wrong - feel free to let me know.

Based on the very good work [here](https://github.com/ckdo/airplay2-receiver).

## Run on macOS

Current process to run on macOS:
```
brew install portaudio
virtualenv proto
source proto/bin/activate
pip install -r requirements.txt
pip install --global-option=build_ext --global-option="-I/usr/local/Cellar/portaudio/19.6.0/include" --global-option="-L/usr/local/Cellar/portaudio/19.6.0/lib" pyaudio


python ap2-receiver.py -m myap2
```

## Protocol notes
 - https://emanuelecozzi.net/docs/airplay2
 - https://openairplay.github.io/airplay-spec