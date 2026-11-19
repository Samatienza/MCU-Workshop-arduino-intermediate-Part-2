## Sequencer Code Activity

The sequencer code that you have been provided with can play several
different melodies using the NOTES and TIMES arrays.

**Activity:**

1.  Download and unzip SYNTH\_SEQUENCER.zip. Inside the SYNTH\_SEQUENCER
    folder, open SYNTH\_SEQUENCER.ino.

2.  In the Arduino IDE, Select the board (Seeeduino Nano) and port and
    upload the code.

3.  Press the buttons to play the programmed sequences. Adjust the
    potentiometers as the sequences are playing and observe how the
    output sounds different.

4.  Choose a sequence that you recognize. Adjust the attack, decay,
    sustain, and resonance to make the sequence sound more similar to
    the original tune. Record the adjustments that you made below.

<table style="width:99%;">
<colgroup>
<col style="width: 99%" />
</colgroup>
<thead>
<tr>
<th><p>The NOTES array contains a set of notes to be played. The TIMES
array is used to store the corresponding times that each note is played
for.</p>
<p>The number of elements in an array is indicated by the number
enclosed in square brackets. This number must match the number of
elements enclosed in the curly brackets. Both arrays must have the same
number of elements.</p>
<p>The notes and times enclosed in the curly brackets are separated by
commas.</p>
<p><img src="./assets/2_F26_TD_Activity/image8.png"
style="width:6.34653in;height:2.36842in" /></p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  Choose a song and instrument that you want to recreate using the synthesizer.
    In SYNTH\_SEQUENCER.ino, edit the NOTES\_3 and TIMES\_3 arrays according to the
    song you would like to play. Usually doing a quick google search can get you the
    musical notes of a particular song. It may also be wise to choose a song
    with a melody that is easy to recognize (ex. nursery rhymes like “Mary had
    a little lamb”). Once you have inputted the new notes and times for
    your chosen song, don’t forget to **change the number of elements**
    when initializing your array (see the number circled below).

    <img src="./assets/2_F26_TD_Activity/image9.png"
    style="width:4.98947in;height:1.8476in"
    alt="A screenshot of a computer Description automatically generated" />

3.  If you wish to have a sequence repeat you must set the
    ‘sequence\_looping\_X’ variable where ‘X’ is the number of the
    sequence to true. If looping you must set the very first note of the
    list to ‘REST’, and the very first time to ‘0’ for the loop to work
    properly.

4.  If you wish to change the type of Oscillator that you are using, you
    can modify the ‘internal.cpp’ file. All you need to do is comment
    out the current oscillator and uncomment the oscillator that you
    wish to use. An image of the section that you can modify is shown
    below:<img src="./assets/2_F26_TD_Activity/image10.png"
    style="width:6.5in;height:1.44653in"
    alt="A screen shot of a computer code Description automatically generated" />

    *Note: If you get an error saying that global variables use more
    than 100% of dynamic memory, try reducing the number of elements in
    your sequences to free up space.*
