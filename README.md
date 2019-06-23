# flexYnth
## A flexible synthesizer development library.
### By Franco Caspe (francocaspe@hotmail.com)

**flexYnth** is a C++ library aimed for multi-plattform synthesizer software development.

The library is divided into two set of base classes called **Engine Scheme** and **Synthesizer Scheme** that once implemented yield a
**Synthesizer Engine** and a **Synthesis Architecture** respectively.

![](img/1.png)

<center> **Example of a Synthesizer and Engine class scheme and some of its members and interaction.** </center>

## Scope
This project is specially developed to ease and somewhat standardize the development of DIY synthesizer boxes based on DSP or
microcontrollers. The idea came while researching onto some nice electronic synthesizer projects out there in the net.
I realized that could be really benefical if there'd be a way to solve the hardware and software implementation separately.

## Features
This repo contains the Synthesizer Scheme and Engine Scheme as well as two separated engines in two branches:

branch **master**: Synthesizer Scheme and Engine Scheme virtual classes only - no implementation whatsoever.

branch **alsa_linux**: An ALSA-BASED PC/Linux Synthesizer Engine for Synthesis Architecture testing.

branch **discovery_f4**: A ST Microelectronics Discovery STM32F407 Board Engine for Synthesis Architecture implementation.

## Usage Examples

- Provided we have a completed **Synthesizer Engine** developed and tested for a specific HW/OS plattform
(i.e.: Arduino box, Custom PCB, PC running Linux) we can implement any existing **Synthesis Architecture** on it.

![](img/2.png)
<center> **Different Synthesis Architectures can connect to an unique Engine at compile time.** </center>

- You may want to expand/simplify an existing Synthesizer Project capabilities, updating the controls, the motherboard, the DAC,
the CPU. In this case you should want to code a new **Synthesizer Engine** following the **Engine Scheme** provided with **flexYnth**.

![](img/3.png)
<center> **HW can be upgraded just by developing a new Engine. (i.e. for polyphony expansion, a new PCB, more inputs, ...)** </center>

- It's easy to develop a **Synthesis Architecture** with the **Synthesizer Scheme** provided with **flexYnth**.
You can take advantage of the existing **Linux Engine** for testing purposes.

![](img/4.png)
<center> **ALSA/Linux Engine allows for out-of-board Architecture debugging.** </center>

## Check out some flexYnth implementation examples!

**bfreeOrgan2**: A Tonewheel Organ Synthesizer

## License

Released under Apache V2.0 License.