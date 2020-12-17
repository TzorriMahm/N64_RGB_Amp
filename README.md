# N64 RGB Amp
**A modding board to achieve RGB video on some early NTSC models by using TI's THS7374 video amplifier.**<br>

![Header image](https://github.com/TzorriMahm/N64_RGB_Amp/blob/master/img_n64/n64_header-wm.png)
<br><br>
**⁓ Designed with ♥ in Germany ⁓**<br><br>
![TzorriMahm](https://github.com/TzorriMahm/N64_RGB_Amp/blob/master/img_n64/tzorri_logo.png)
# Where to get the PCB?
You can order the PCB directly from [OSHPark](https://oshpark.com/shared_projects/cdlxvTEA).
Of course, feel free to use the gerber files with any manufacturer of your choice.<br>
Use 0.8mm board thickness to ensure an easy and clean installation.

# Before you start
**This modification only works with NUS-CPU-01/02/03/04 main board revisions!**<br>
Also, verify that your main board has a 'VDC-NUS'/'VDC-NUS A' chip (U4).<br>
If that's not the case - **stop here!** Your console is not compatible with this modding board!

![VDC-NUS](https://github.com/TzorriMahm/N64_RGB_Amp/blob/master/img_n64/vdc-nus-wm.jpg)

# Install instructions
## Bottom metal shielding
Use a pair of pliers to bend away the tab which is located at the MultiOut area.<br>
This avoids the shielding from hitting the modding board later.

![Bottom metal shielding](https://github.com/TzorriMahm/N64_RGB_Amp/blob/master/img_n64/bottom_shielding-wm.jpg)<br>

## Preparing the N64 main board
- remove R1, R14, R15, R16, C22

## Installing the modding board
- isolate the bottom side of the modding board to avoid any shorts
- solder the modding board onto the pins of the MultiOut
- solder a wire from the via next to R8 (N64 main board) to pad 'R' (modding board)
- solder a wire from the via next to R9 (N64 main board) to pad 'G' (modding board)
- solder a wire from the via next to R10 (N64 main board) to pad 'B' (modding board)
- solder a wire from the via next to R16 (N64 main board) to pad 'CS' (modding board)<br>

## Install diagram
![Install diagram](https://github.com/TzorriMahm/N64_RGB_Amp/blob/master/img_n64/n64_dia-wm.png)

# Troubleshooting
Double-check continuity between connections:
- 'R' (modding board) ⇄ VDC-NUS(A) pin 17 (N64 main board)
- 'G' (modding board) ⇄ VDC-NUS(A) pin 19 (N64 main board)
- 'B' (modding board) ⇄ VDC-NUS(A) pin 21 (N64 main board)
- 'CS' (modding board) ⇄ VDC-NUS(A) pin 14 (N64 main board)


**Check for shorts to VDC-NUS(A)!** The vias you solder to are located directly beneath that IC.<br>
It's ridiculously-simple to short something when the exposed conductors are a little bit too long!

# Miscellaneous
#### Jumper 'J:LPF'
The THS7374 has a low pass filter on each of the four channels which can be turned on by shorting jumper 'J:LPF' on the modding board. This is mostly needed if you wire the console directly to a flat-screen TV. There's no need for the low pass filter on analogue devices.<br>
If you use an OSSC or a Framemeister, it's better to use their filter options.

#### RGB cable
You will need a RGB cable with 220µF electrolytic capacitors on each of the 'R', 'G' & 'B' lines. The positive end is facing towards the console.<br>
This modding board is designed to output TTL level C-Sync directly at the MultiOut of the console.<br>
With that in mind, make sure you're using a suitable cable with a 470Ω resistor on the sync line to use it with most consumer products (like TV's, OSSC, Framemeister)!

# Disclaimer
I am not responsible for any damage to you, your devices or anything else!<br>
If you do the modification, you do it at your own risk and responsibility!

# Acknowledgement
Most of the credits should go to [borti4938](https://github.com/borti4938). He has made the actual (slightly different) circuit and inspired me to design this board. Thanks man! Thanks Bob, for your awesome and informative website [RetroRGB](http://retrorgb.com)!<br>
And of course, thanks to the whole retro gaming community for keeping the spirit alive!
