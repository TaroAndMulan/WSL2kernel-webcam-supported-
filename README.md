# WSL2kernel-webcam-supported-

WSL2 does not support webcam by default. You have to build a custom linux kernel yourself.

This repositories provide a ready to use WSL2 kernel images for those who don't want to build a kernel manually.

You can follow an instruction from this video.  [youtube_instruction_by AgileDevArt](https://www.youtube.com/watch?v=t_YnACEPmrM)

He built a kernel from minute 3.00 - 6.40, resulting in an kernel image name "vmlinux". If you don't want to build it yourself, you can download my "vmlinux" and place it on C:\\Sources manually. 

## Gdrive link for kernel
Based on [linux-msft-wsl-6.6.36.3](https://github.com/microsoft/WSL2-Linux-Kernel/releases/tag/linux-msft-wsl-6.6.36.3). The youtube guide used an old version 5.15.57.1.

vmlinux https://drive.google.com/file/d/1_PsVRgl04gyvajecYfomNu5nRT_PRIuV/view?usp=sharing.

## Note on openCV (python)
I have to set a videocapture with an additional flag (cv2.CAP_PROP_FOURCC); otherwise, it won't work.
```
import cv2
cam = cv2.VideoCapture(0)
cam.set(cv2.CAP_PROP_FOURCC, cv2.VideoWriter_fourcc('M', 'J', 'P', 'G'))
```
