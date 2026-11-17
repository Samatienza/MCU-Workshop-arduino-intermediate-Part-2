The synthesizer you will be creating has two modes that you can switch
between by pressing a button. One mode is called the ‘**LFO state**’,
while the second mode is ‘**ADSR state**’.  These modes are controlled
by potentiometers.

- ‘LFO state’ potentiometers

  - Waveform (sine, triangle, saw, and square waves)

  - Frequency/Pitch

  - Cutoff/Intensity

  - LFO Cutoff rate

  - Resonance (i.e. the vibrating quality of the sound)

  - Amplitude/volume

- ‘ADSR state’ potentiometers

  - Attack 

  - Decay 

  - Sustain 

  - Release

The basic design of the synthesizer also includes one button that will
play a single note according to attack, decay, sustain, and release
values. If you haven’t watched it already, [this
video](https://youtu.be/mKSo2ANMSEE?si=SVDKjxPIVjyonnV4)—which was
linked in the prerequisites document—is helpful in understanding more
about how ADSR works and sounds.

The teaching team will provide you with the following parts to construct
the synthesizer. Before you begin, please ensure that you have all of
the materials listed below:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr>
<th>Component Name</th>
<th>Number of Components</th>
</tr>
</thead>
<tbody>
<tr>
<td>Seeeduino Nano</td>
<td>1</td>
</tr>
<tr>
<td>PCB</td>
<td>1</td>
</tr>
<tr>
<td>USB-C Cable</td>
<td>1</td>
</tr>
<tr>
<td>Cardboard Speaker Cab Design (from Day 1)</td>
<td>1</td>
</tr>
</tbody>
</table>

You have also been provided with the following project folders, which
you will need to use to run your synthesizer:

- PCB\_CONNECTION\_CHECKER

- SYNTH\_BASE

- SYNTH\_SEQUENCER

First, let’s ensure that each button and potentiometer is properly
soldered to the PCB. The PCB\_CONNECTION\_CHECKER.ino code reads the
values from the digital pins and prints them to the serial monitor.

1.  Download and open PCB\_CONNECTION\_CHECKER.ino. After the IDE opens,
    a popup window may appear, prompting you to create a new folder to
    store your project in. Choose ‘**Ok**’.

2.  Using the provided USB-C to USB-A cable, plug your Seeeduino Nano
    into your computer.

3.  Select the appropriate board and port that you will be uploading
    your code to. From the ‘**Select Board**’ dropdown menu, choose
    ‘**Select Other Board and Port**’ and choose ‘**Seeeduino Nano**’.
    Select the port that appears in the ‘**Ports**’ menu, then select
    ‘**OK**’ to close the pop-up window.

4.  Ensure that the code compiles using ‘**Verify**’ check mark button.
    If there are no error messages, proceed by sending the code to the
    synthesizer using the ‘**Upload**’ arrow button. A message should
    appear in the Output once the upload has finished.

5.  Open the Serial Monitor using ‘**Ctrl**’ + ‘**Shift**’ + ‘**M**’ or
    ‘**Command**’ + ‘**Shift**’ + ‘**M**’. Try turning the dials on each
    potentiometer and pressing each button.

The value associated with the first five potentiometers should increase
as the dial is turned clockwise and decrease as the dial is turned
counterclockwise. The button states should be ‘0’ (low) when pressed and
‘1’ (high) when not pressed. It might be a good idea to add a delay
after the print commands so that you are able to read the values shown
on the Serial Monitor \[ex. delay(3000);\]. If your PCB is not behaving
as expected, consult a member of the teaching team before proceeding to
the activity.
