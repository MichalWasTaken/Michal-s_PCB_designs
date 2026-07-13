# Michal-s_PCB_designs
Repo for collecting and describing my PCB designs

I am also actievely developing a gas analyzer project, where I'm making a shield for and STM32 nucleo board as a stepping stone towards a stand-alone system. For this one I'm trying to learn KiCad, and so I can actually use GIT for version control. Here is the link to that repo: https://github.com/MichalWasTaken/STM32Sheild.git

**Quick description of each PCB:**

**Bachelor buck covnverter:**

  This PCB worked very well, converting 50V to 16.8V at a max current of around 3A, and achieving an efficency of around 95%.
  It had some thermal issues though (especially at high currents), nothing outside of the comonent limits, but some optimazations could be done.

**Bachelor Coulomb counter:**

  This PCB used the LTC2959 coulomb counter IC to measure the state of charge, voltage, and current from a battery. An MCU (for out project an           AVR128DB48 on a curiosity nano board) was used to communicate with the coulomb counter via I2C to read its internal registers and to perform state of charge calculations. With this PCB i also learn the hard way why reverse polarity and ESD protection is useful, as a destroyed 2 versions of this PCB with (you guessed it) connecting the power supply in reverse, and with ESD.

**Dive light:**

  I was making a diving light, with the battery and light head in separate compartments. I made 2 PCB's: one battery compartment serving as the master   side, and one in the light head compartment serving as the slave side. Both PCB's were equipped with an ATTINY1604 MCU and power line communication     IC. Ultimately this project was left on the shelf, mainly due to a few findamental errors early on in the project, and to some extend lack of time. 

**Vortex acoustic preampt/filter circuit:**

  This PCB was to take in a weak (in the mV range) signal at a frequency of 20-40 kHz, filter out all the unwanted signals and amplify the wanted       ones. This was acheived in 2 stages; the 1st was an instrumentation amplifyer, which filters out common noise and was the main amplifying stage,        followed by a bandpass filter consisting of a cascaded low and high pass filter. While I mostly completed the desing, I was not able to follow          through with the prdouction and testing, since I was starting my fulltime position at Nordic Semi at the time. I did spend a lot of time simulating   this circuit in LTSPice, where it performed excellently.
