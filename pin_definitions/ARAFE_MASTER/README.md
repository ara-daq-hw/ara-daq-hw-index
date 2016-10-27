# Energia and ARAFE_MASTER

Energia has base support for the MSP430FR5739. It is either called a
"FraunchPad" (in older Energia installs) or MSP-EXP430FR5739LP.

The pins_energia.h file however is missing a bunch of functions. In
the Energia install, find the existing pins_energia.h file in
either hardware/msp430/variants/fraunchpad/pins_energia.h, or
hardware/energia/msp430/variants/MSP-EXP430FR5739LP. Replace it with
the file in this directory.

Note that unless you use the MSP-EXP430FR5739 as a programmer, you may not
be able to use the 'Upload' command on Energia. In that case, you can just
do Sketch->Export compiled Binary, and use a standalone programmer (e.g.
FET-Pro430 Lite) to program the hex file directly. Note that the ARAFE Master
uses Spy-Bi-Wire for JTAG communication, so make sure that is selected in
"Setup->Connection/Device Reset".
