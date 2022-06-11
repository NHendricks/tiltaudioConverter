# tiltaudioConverter
Converts Audio-Packs using Altsound to Tiltaudio-Format.

Please install java and set JAVA_HOME. Then run [gradew.bat|gradlew] tasks.
The first call will download a gradle runtime into the gradle cache (to <home>/.gradle). Subsequent calls will be faster.

To generate code run [gradew.bat|gradlew] generate.


How it works:
It just reads the tiltaudio.csv file from the _input-directory and copies all altsound files over to the structure tiltaudio needs. In further steps this generator might simply convert the random-number-foldernames of a pinsound-zip into foldernames that tiltaudio will understand.