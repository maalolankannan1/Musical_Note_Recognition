# PIANO NOTES RECOGNITION 
Music is an integral part of everyone’s lives. Music helps in relaxation, therapy and entertainment. 
The audio industry is booming with online platforms for music streaming. This program helps identify the musical notes in a piece of audio and gives valuable information about its pitch, frequency and type. 
The music piece fed to the system can be decoded to identify which note the signal corresponds to.

## THE BLOCK DIAGRAM
![block](https://user-images.githubusercontent.com/42891566/94290918-832acc80-ff78-11ea-9338-8b83b2aa7624.JPG)

The musical piece or audio file containing a note is fed to the system which processes the audio signal and recognizes the frequency and pitch of the signal. 
Fast Fourier Transform is then applied to get the maximum amplitude which corresponds to the fundamental frequency of the note,  thereby identifying the type of musical note by comparing it with the frequencies of standard musical notes available.

## To Use:
Change the .wav file in the audioread() function of noteparsem.m file and run

## FUTURE WORK:

There is still much room for future development that would enhance the system and increase its usage value. The following items are some suggestions:
-	**Advanced Note Detection:**   
There are lot of ways we to improve and customize note detection. Most of them use variations in intensity, which is not the right way because strictly speaking a note is said to change when the frequency of the signal changes. It is not easy to keep track of change in frequency because the change is gradual and hence it is an existing challenge. Moreover the frequency estimation for calculating note detection requires note detection in a crude sense which is paves way for development in this area.

-	**Non Periodic Signal analysis:**  
The process is relatively simple if the signal were sinusoidal or periodic. But the real life musical notes or vocals are approximately periodic and the frequency itself changes with time because a sample may contain more than one note and that is how music is played. While Fourier Analysis is a nice solution to this problem, it is not sufficient. Theoretically it may be sufficient but its high level implementation is not as there is resolution and run time limit. There is scope to overcome latter by designing algorithms especially for the purpose of frequency estimation and not focusing on phase detection.

-	**Multiple Notes at a time:**   
Our project assumes that only a single note is played at a time. But that is not it. We can develop it further by using Fourier Analysis again. There are existing algorithms which can isolate multiple notes. After splitting the audio sample into individual notes we can apply our own techniques to find the frequency.

