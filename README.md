# Web MIDI Extension for Scratch3
    
  
This extension is for using a MIDI device like a MIDI Controller through Scratch3. It's made by Web MIDI API. This API is one of the HTML5 functions defined by W3C.  
  
  
Application page is [Web MIDI Scratch 3](https://masahirokakishita.github.io/scratch3webmidi/)  
  
  
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

- Open Scratch 3 Editor from [here](https://masahirokakishita.github.io/scratch3webmidi/)
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

### Note On Message

- ![alt](pict/message.jpg)<br>
Genarates a MIDI NOTE ON message. The first parameter is a channel number, the second one is a note number and last one is a velocity. Normary the velocity is zero means note off. 




