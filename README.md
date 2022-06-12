# tiltaudioConverter
Converts Altsound-Audio-Packs to Tiltaudio-Format.

Please install java and set JAVA_HOME. Then run [gradew.bat|gradlew] tasks.
The first call will download the gradle runtime into the gradle cache (to <home>/.gradle). Subsequent calls will be faster.

To generate tiltaudio from altsound run gradew.bat generate

To convert ogg files to wav run gradew.bat convert

How it works:

1. generate:
It just reads the tiltaudio.csv file from altsound.zip in the directory "_input" and copies all altsound files over to "_output" into the directory structure tiltaudio needs. In further steps this generator might simply convert the random-number-foldernames of a pinsound-zip into foldernames that tiltaudio will understand.

2. convert:
It uses your installation of ffmpeg in the directory "_ffmpeg", converts and normalizes the .ogg files to .wav files
If the conversion has a problem maybe the file name is too long. Place this tool at c:\tiltaudioConverter or reduce the filename length. The ogg-Files will be deleted so subsequent calls will only retry converting the remaining files.
