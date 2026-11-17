## Additive Synthesis

Delete the existing Audacity rack lists to start with an empty project.
Making sure that they’re on different track lists, generate two tones
according to the following specifications:

- Sine wave with frequency **523 Hz**, amplitude of **0.5**, and
  duration of **2 seconds**

- Sine wave with frequency **784 Hz**, amplitude of **0.5**, and
  duration of **2 seconds**

Try playing each tone separately by spacing them out and listening to
them separately.

Notice that the two sounds create a ‘bigger’ sound when played together.
This is because of a concept called **superimposition**. When multiple
tones are played at the same time, the sound you hear is the sum of each
pure tone. Mathematically, this can be observed by adding the waveform
functions together in graphing software such as
[Desmos](https://www.desmos.com/calculator).

Place both tones on top of each other and play to listen to them at the
same time.

The 523 Hz and the 784 Hz tones complement each other to create a
pleasant, harmonized sound when played together.

## Synthesizer Envelopes – Non-Constant Amplitude + Frequency

In the previous section, we heard a sine function with a time-varying
amplitude. We can use different functions to modify the amplitude over
time, and we can also have time-varying frequencies!

We can replace the non-constant amplitude from the beats section,
${2Acos\left( \left( \frac{w1 - w2}{2} \right)t \right)\sin}\left( \left( \frac{w1 + w2}{2} \right)t \right),$
with a decaying exponential such as
${16e}^{( - 6\*t)}\sin\left( \left( \frac{w1 + w2}{2} \right)t \right)$
. This will make the sine function look and sound different since the
amplitude (and consequently, the volume) of the note decreases as the
note is playing. Below are some visual examples:

<img
src="./assets/3_F26_TD_Manipulating_Sound_Waves/media/image2.png"
style="width:2.56904in;height:1.48947in"
alt="A picture containing letter Description automatically generated" />
<img
src="./assets/3_F26_TD_Manipulating_Sound_Waves/media/image3.png"
style="width:2.5761in;height:1.52038in"
alt="A picture containing text Description automatically generated" />

Non-constant Amplitude

Now we can apply the same concept for the frequency of a sine function.
Recall the general equation of

a sine function, *y* = *A**s**i**n*\[ *ω*(*x* − *C*) \] + *D*, and that
the period of the function is given by
$\frac{\mathbf{2\pi}}{\omega}$**.** The angular frequency, *ω*, has a
reciprocal relationship to the period. This means that a small period
corresponds to a high frequency. Altering the frequency of the sine
function will result in a non-constant frequency which will cause the
pitch to fluctuate.

Did you know we can create drum-like sounds with this method? When the
frequency is defined by a decaying exponential, it causes a sharp drop
in the pitch which results in a drum-like sound. Below is a visual
example:

<img
src="./assets/3_F26_TD_Manipulating_Sound_Waves/media/image4.png"
style="width:2.61736in;height:1.55456in"
alt="Shape Description automatically generated with medium confidence" />

Non-constant Frequency

[Click here](https://youtu.be/ogFAHvYatWs?t=255) to listen to the sounds
produced from the non-constant amplitude and frequency.

Various non-constant functions can be used to define the frequency of a
wave. While a sinusoid amplitude produces a pulsing sound, a sinusoid
amplitude creates a “siren” type sound. You can observe the low and high
frequencies of a sinusoid frequency below:

<img
src="./assets/3_F26_TD_Manipulating_Sound_Waves/media/image5.png"
style="width:6.5in;height:1.53889in"
alt="A picture containing text, shoji, building Description automatically generated" />