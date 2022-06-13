# tiltaudioConverter
Converts Altsound-Audio-Packs or Pinsound-Audio-Packs to the ordered folder structure for Tiltaudio to get a unified format so that changes can be applied more easily.

Please install java (or make sure that the environment variable JAVA_HOME is set correctly). Then run gradew.bat tasks.
The first call will download the gradle runtime into the gradle cache. Subsequent calls will be faster.

To generate from Altsound-zipfile into tiltaudio (ordered) directory structure run "gradlew.bat generateAltsound2Tiltaudio"

To generate pinsound randomized directories into tiltaudio (ordered) directory structure run "gradlew.bat generatePinsound2Tiltaudio"

To convert and normalize ogg files to wav run "gradlew.bat convert"

How it works:

1a. generateAltsound2Tiltaudio:
It reads the altsound.csv file from _input/<altsound.zip> and copies all sound files to the _output directory.

1b. generatePinsound2Tiltaudio:
As an alternative to 1a it reads the altsound.csv file from _input/<altsound.zip> and copies the corresponding sound files from _input_pinsound/<pinsound.zip> to the _output directory.

2. convert:
It uses your installation of ffmpeg in the directory "_ffmpeg", converts and normalizes the .ogg files to .wav files
If the conversion has a problem maybe the file name is too long. Place this tool at c:\tiltaudioConverter or reduce the filename length. The ogg-Files will be deleted so subsequent calls will only retry converting the remaining files.
