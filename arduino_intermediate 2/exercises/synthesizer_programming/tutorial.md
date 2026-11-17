## Synthesizer Base Code Activity

You have been provided with a .zip file called SYNTH\_BASE.zip. Within
this .zip file, there is starter code that can be run on your
synthesizer. The folder also contains .cpp and .h files which define
several functions and variables used in the code. During this activity,
only edit the SYNTH\_BASE.ino file.

1.  Download and unzip SYNTH\_BASE.zip. The steps to unzip a .zip file
    depend on your operating system.

2.  Inside the SYNTH\_BASE folder, open SYNTH\_BASE.ino. Select the
    board (Seeeduino Nano) and port and upload the code.

3.  Test out the synthesizer by pressing the buttons and adjusting the
    potentiometers. Based on your observations and the provided code,
    determine the function potentiometer and button. Record the
    function(s) associated with each component in the table below (if
    there are no associated functions, write ‘N/A’).

    *Note: It may be helpful to open the Serial Monitor (Ctrl + Shift +
    M or Command + Shift + M) to monitor status messages.*

*  *

<table style="width:99%;">
<colgroup>
<col style="width: 13%" />
<col style="width: 3%" />
<col style="width: 8%" />
<col style="width: 7%" />
<col style="width: 3%" />
<col style="width: 13%" />
<col style="width: 13%" />
<col style="width: 3%" />
<col style="width: 8%" />
<col style="width: 7%" />
<col style="width: 3%" />
<col style="width: 13%" />
</colgroup>
<thead>
<tr>
<th colspan="2" style="text-align: center;"><strong>A:</strong></th>
<th colspan="2" style="text-align: center;"><strong>B:</strong></th>
<th colspan="2" style="text-align: center;"><strong>C:</strong></th>
<th colspan="2" style="text-align: center;"><strong>D:</strong></th>
<th colspan="2" style="text-align: center;"><strong>E:</strong></th>
<th colspan="2" style="text-align: center;"><strong>F:</strong></th>
</tr>
</thead>
<tbody>
<tr>
<td colspan="12" style="text-align: center;"><img
src="./assets/2_F26_TD_Activity/media/image6.png"
style="width:6.3125in;height:4.66807in" /></td>
</tr>
<tr>
<td style="text-align: center;"><strong>G:</strong></td>
<td colspan="2" style="text-align: center;"><strong>H:</strong></td>
<td colspan="2" style="text-align: center;"><strong>I:</strong></td>
<td style="text-align: center;"><strong>J:</strong></td>
<td style="text-align: center;"><strong>K:</strong></td>
<td colspan="2" style="text-align: center;"><strong>L:</strong></td>
<td colspan="2" style="text-align: center;"><strong>M:</strong></td>
<td style="text-align: center;"><strong>N:</strong></td>
</tr>
</tbody>
</table>

The \#define component is used to name a value that is constant (i.e.,
will not be changed while the program is being run). When the name is
used in code, the compiler replaces the name with its associated value.
Change ‘#define ADSR\_NOTE\_0 7’ line to ‘#define ADSR\_NOTE\_0 2’.
Save, verify, and upload your code to the Seeeduino Nano.

1.  How has this change affected the functionality of the synthesizer?

Currently, the note that can be played in ADSR mode (by pressing one of
the buttons) is set up using the following lines of code:

<table style="width:99%;">
<colgroup>
<col style="width: 99%" />
</colgroup>
<thead>
<tr>
<th><ol type="A">
<li><p>A #define statement that defines the digital pin number (see
<strong>line 22</strong> in the provided code file)</p></li>
</ol>
<p>#define ADSR_NOTE_0 7</p>
<ol start="2" type="A">
<li><p>Declaration of a bool variable to store the current state of the
button, set to high to start (see <strong>line 39</strong> in the
provided code file)</p></li>
</ol>
<p>bool notePinState0 = HIGH;</p>
<ol start="3" type="A">
<li><p>A pinMode statement that defines an input in the setup function.
The pinMode function defines the ADSR_NOTE digital pin (D3) as an input
(see <strong>line 60</strong> in the provided code file)</p></li>
</ol>
<p>pinMode(ADSR_NOTE_0, INPUT_PULLUP);</p>
<ol start="4" type="A">
<li><p>A case that uses digitalRead to read the current state of digital
pin 3 (D3) in the checkInputs function (see <strong>lines 91 and
92</strong> in the provided code file)</p></li>
</ol>
<p>case 0:</p>
<p>notePinState0 = digitalRead(ADSR_NOTE_0);</p>
<p><strong>Note</strong>: when adding additional notes, you will have to
make another case (i.e case 1, case, 2, case 3, etc.).</p>
<ol start="5" type="A">
<li><p>A line to call the updateADSR function to play notes based on
recorded input of all the buttons. This function can update the ADSR
mode based on up to 6 pin states (see <strong>line 122</strong> in the
provided code file)</p></li>
</ol>
<p>updateADSR(notePinState0);</p>
<p>For example, if you want to use three pin states, you would make the
following changes:</p>
<p>updateADSR(notePinState0, notePinState1, notePinState2);</p></th>
</tr>
</thead>
<tbody>
</tbody>
</table>

1.  Using the 5 steps outlined above, add new code to SYNTH\_BASE.ino
    that will allow you to play **six** different notes. Hint: simply
    create a new variable for each new note that you will make (step A),
    and use the rest of the steps above like a recipe to set up each
    note. For each new note, you will have to create a new variable name
    and specify a **different** digital pin number. Reference the PCB
    image below to see which digital pins correspond to which buttons
    (ex. to have **button K** play a note, you will need to connect it
    to **digital pin 5**)

> <img src="./assets/2_F26_TD_Activity/media/image7.png"
> style="width:4.51123in;height:3.42632in"
> alt="A close up of a circuit board Description automatically generated" />

*Note: It may be easier to start by modifying the code to play only two
different notes.*

