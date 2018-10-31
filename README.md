# ratiometric

How to make ratiometric measurements with a microcontroller and ADC.
We will be developing a circuit including an analog multiplexer, ADC and microcontroller to allow us to make precision measurements of resistance or inductance, and maybe even capacitance, referenced to one or two stable resistors, which
are more consistently accurate than seniconductor voltage references. We will also introduce means of self-testing the
system to ensure that there are no errors due to ADC bit failures etc. Averaging will be used over a full cycle of 50Hz
or 60Hz mains frequency to reduce the major source of noise.

Note that hardware experience will be required to implement what will be published here, and it may be that PCBs
will be available.

It is likely, but not yet decided, that a TMS570 Hercules development board will be used rather than an Arduino as
32 bit arithmetic is going to be necessary, and I happen to have some of these. However the code will be written in C
and should be portable to anywhere that can do hard real time and perform fixed point multiply/accumulate in acceptable time.

The techniques herein will be based on those used in certain safety-critical systems, however the use of a "safety"
microcontroller is purely coincidental and in itself does not make a safe product. If you wish to use any of the techniques
which you may learn here in a safety system you must design the entire system accordingly and go through all the neccessary
certicication procedures.

There will be optional electrical isolation between the computational components (microcontroller etc) and the analog data
acquisition circuits and therefore it will be possible to use the design in situations where electrical isolation is required. 
However, electrical safety depends on correct construction and usage, in accordance with local regulations, and you must attend
to this yourself.

NEITHER ANY CONTRIBUTOR TO THIS GITHUB PROJECT NOR THE ORGANISATION BEHIND GITHUB HAVE ANY KNOWLEDGE OF AND PROPOSED END
USES OF ANY TECHNOLOGY PRESENTED HEREIN AND WILL NOT UNDER ANY CIRCUMSTANCES BE LIABLE FOR ANY EVENT INCLUDING  BUT NOT
LIMITED TO ACCIDENT, LOSS, MISHAP OR FAILURE TO PERFORM.  THERE IS NO WARRANTY WHATSOEVER. USE AT YOUR OWN RISK ONLY.

The initial developer is using UK safety and other regulations, and anything that is contributed must comply with English law.
Disputes are for the English legal system to resolve. 

Contributions will be welcome once the project is at a sufficiently mature and stable state. NOT YET PLEASE! Contributors are responsible for the legality of their own contributions and may only submit code and other information where they have the
legal rights to do so.


