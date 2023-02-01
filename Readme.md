Whisper AI
https://github.com/openai/whisper for reference



Whisper is a general-purpose speech recognition model. It is trained on a large dataset of diverse audio and is also a multi-task model that can perform multilingual speech recognition as well as speech translation and language identification.


easy and errorless way to setup the project


step 1.
install python>=3.7




step 2
create an virtual environment (its imp if you wany use different version on different project and also help in deyployemnt 


```
pip install virtualenv
virtualenv myproject
source myproject/Scripts/activate
```

step 3 (for the use of Gpu)
install latest pytorch tool kit from  https://pytorch.org/get-started/locally/
try not to go for python 3.9+ yet its may possible to give cuda error

step 4 
install Whishper

```
pip install git+https://github.com/openai/whisper.git 

```

step 5
install ffmpeg 

best way without getting ffmpeg error is to download from the site 
https://ffmpeg.org/

after download extract and put the files in bin folder in the project folder

step 6 
download yt-dlp https://github.com/yt-dlp/yt-dlp/releases/tag/2023.01.06 to download youtube file where you want the transcribe
after download extract and move the exe file in project folder


step  7 
convert video into audio using ffmpeg

```
ffmpeg....
```

step 8 

now we will transcribe the audio using Whisper
```
whisper <videoname>.<file format> --language <video language> --model large  --task transcribe --device cpu -o 'output directory path' 
```
you can change cpu to gpu by changing cpu in code to cuda

step 9 
```
whisper <videoname>.<file format> --language <video language> --model medium   --task tranlate --device  -o cuda 'output directory path' 
```
translate always traslate from any language to english laguage
while in transcribe you can output in the same audio language

if you not predefine the audio laguage (--language) it will automatically detect the the language and trancribe for only 30 sec



