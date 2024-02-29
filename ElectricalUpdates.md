**2/28 Update**


This week I'm figuring out how to get rid of electrical noise in our system. We have noticed certain noise with the daisy seed when the seed is unplugged, and the USB is touched, and also some additional noise while the seed is plugged into a computer. We have notice decent reduction in noise when using a powerbank, but we would like to make our system a bit more robust.

This is the process I'm planning to go through this week to tackle this problem. 

1. Plug seed into laptop, and connect input and outpin pins to oscilliscope. Determine frequency of noise. Determine frequency of transmission line noise. 
2. Implement a software filter using [this filter] (https://electro-smith.github.io/DaisySP/classdaisysp_1_1_one_pole.html) This probably won't work because this issue persists even when daisy is unpowered, but I would like to see what it does. 
3. Implement a [hardware filter on the output pin] (https://www.arrow.com/en/research-and-events/articles/using-capacitors-to-filter-electrical-noise). 
4. Power daisy seed with standard 9 external power source. [According to this documetation, the daisy seed can take an input between 4v-17v] (https://daisy.nyc3.cdn.digitaloceanspaces.com/products/seed/Daisy_Seed_datasheet_v1.0.6.pdf) This may induce low frequency electrical noise, and if it does, I can add a HPF on the input power pin. This may address output gain issues. If this does, great! If it doesn't I plan to implement an amplifier circuit on the output.


As I work through these steps, I will publish my results here. 
