# Explanation for Scratch 3 MIDI


This extension is for using a MIDI device like a MIDI Controller through Scratch3. It's made by Web MIDI API. This API is one of the HTML5 functions defined by W3C.  


Application page is [Web MIDI Scratch 3](https://UchiwaFuujinn.github.io/scratch3webmidi/)  


### Reference
- [Web MIDI API Working Draft](http://www.w3.org/TR/webmidi/)
- [W3C](http://www.w3.org/)  
  
## Preparation

__Please Use Chrome.__ This extension is able to use only on Chrome. The other browsers are not supporting Web MIDI API now, April 2016. 
Do you know MIDI? MIDI is a protocol for connecting between MIDI Devices or a MIDI device to the PC. If you don't know, please see like a following page.


- [MIDI wiki](https://en.wikipedia.org/wiki/MIDI)
- [SUMMARY OF MIDI MESSAGES](https://www.midi.org/specifications)


Before you try to use these extensions, you should connect a MIDI device to your PC via USB. After you connect a MIDI device, you launch Chrome browser. Because Chrome browser finds the MIDI device when it launches. 

## Usage

- Open Scratch 3 Editor from [here](https://UchiwaFuujinn.github.io/scratch3webmidi/)
- Push the under-left icon.

![alt](pict/webmidi003.jpg)

- Select Web MIDI Extension form Extension list

![alt](pict/webmidi001.jpg)

- You can find Web MIDI blocks under the block paret.

![alt](pict/webmidi002.jpg)

### HAT Block

- ![alt](pict/hat01.jpg)
indicates all midi event

- ![alt](pict/hat02.jpg)
indicates note on event

- ![alt](pict/hat03.jpg)
indicates note off event

- ![alt](pict/hat04.jpg)
indicate pitch bend event

- ![alt](pict/hat05.jpg)
indicate program change event

- ![alt](pict/hat06.jpg)
indicate control change event

- ![alt](pict/hat07.jpg)
indicates note on event with note number

### reporter block

- ![alt](pict/rep01.jpg) Note Number

- ![alt](pict/rep02.jpg) Velocity

- ![alt](pict/rep03.jpg) Pitch Bend

- ![alt](pict/rep04.jpg) Control Change Value

- ![alt](pict/rep05.jpg) Program Number

### Boolean reporter

- ![alt](pict/event.jpg) MIDI event

  - 'key on' --- key on event
  - 'key off' --- key off event
  - 'cc-chg' --- control change event
  - 'p-bend' --- pitchbend event
  - 'pg-chg' --- program change event

### Note On/Off Message

- ![alt](pict/message01.jpg)<br>
Generates a MIDI NOTE ON message. The first parameter is a channel number, the second one is a note number and last one is a velocity. Normally the velocity is zero means note off. 
- ![alt](pict/message02.jpg)<br>
With duration (continuous time), Generate a MIDI NOTE ON message. The last message is duration. The other parameters are same as above.
- ![alt](pict/message03.jpg)<br>
  Generates a MIDI NOTE OFF message. The first parameter is a channel number, the second one is a note number and last one is a note off velocity. However few instrument adopt note off velocity. 

### Program Change Message

- ![alt](pict/message04.jpg)<br>
First parameter is a channek number, the second one is program number.

### MIDI Output Device Number Select
- ![alt](pict/message06.jpg)<br>
This message is a special message to select MIDI Output Device. If multiple MIDI devices are connected by your computer, you can select which device you send MIDI message.

## BEAT
The bellow messages are for "beat" and tick". 
- ![alt](pict/hat08.jpg)<br>

"beat" means timing signal of a quarter note. This hat code generates a pulse for each beat. And the parameter means Tempo. Tempo means the number of quarter notes while one minute. In this case, tempo=120, one time of each 500msec, the pulse is generated. 

- ![alt](pict/rep07.jpg)<br>

"tick" indicates a position of inside of a bar. In this extension, a quater note is as 480 ticks. So one bar is 1920 ticks. This reporter block displaies from 0 to 1920 cyclically..

- ![alt](pict/message05.jpg)<br>
Wait for time of parameter ticks to run the next command.



