# AI Virtual Volume Control Using Hand(Jupyter Notebook)
This project is about controlling your systems volume using hand with the help of hand tracking module.
AI Virtual volume control by Using Hands Point to detect the movement of hands.

![alt text](https://mediapipe.dev/images/mobile/hand_landmarks.png)


## Needed Libraries 
CV2
MediaPipe
autopy

## Working
### This code is used to use your system volume to be control by hand tracking point of tip finger's top(4) and middle finger's top(12).

from ctypes import cast, POINTER
from comtypes import CLSCTX_ALL
from pycaw.pycaw import AudioUtilities, IAudioEndpointVolume
devices = AudioUtilities.GetSpeakers()
interface = devices.Activate(
    IAudioEndpointVolume._iid_, CLSCTX_ALL, None)
volume = cast(interface, POINTER(IAudioEndpointVolume))
volume.GetMute()
volume.GetMasterVolumeLevel()
volRange=volume.GetVolumeRange()

### Now use hand trakcing module 
if you are working on Pycharm then you can directly use Hand tracking module But i have done my project 
on jupyter notebook by using code snippet of hand module.
