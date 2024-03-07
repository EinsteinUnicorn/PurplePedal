**2/28 Update**

To start, I am planning on creating a code file that daisyseed effects from the DSP library can be pulled from and dropped into. This file will include functional LED and POT integration. I will use a phasor to start

**3/6 Update**

Took a stab at creating a phaser effect that had hardware integration and learned so much about what the Daisyseed library can do.

Noteable changes:
+ AudioCallback function does not need to be in the continous while loop within the main function to run
+ increased the volume by multiplying the output by a gain factor
+ In this example I am multiplying the input signal by the phasor effect, previously we passed the input into the phaser.Process function. This change should be explored a bit more to decide what is best
+the while loop is now used only to update the LED and Button states, this will also be the place to update the POT reading

Next steps:
+ integrate a potentiometer to adjust the frequency of the phasor effect

