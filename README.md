# Monte Carlo Multi-Layered (MCML)

The MCML program was created in 1994 by Lihong Wang and Steven Jacques while they worked together at the University of Texas M. D. Anderson Cancer Center, in the Laser Biology Research Laboratory. The program allows multiple planar layers of tissue, each with different optical properties (μa, μs, g, n) and thickness.

The work was based on the previous work by Marleen Keijzer, Scott Prahl and Steven Jacques, but added the feature of multiple tissue layers.

A companion program called CONV provides convolution of MCML output files against flat-field or Gaussian-shaped spatial beam profiles


## MCML source code in ASCII

Individual files in ASCII text format can be downloaded:

mcml.h, 6K, is a header file with data structures and declarations.

mcmlio.c, 26K, contains routines for I/O functions.

mcmlnr.c, 2K, contains some special routines such as error report and array declaration and release.

mcmlgo.c, 19K, contains routines that launch, move, and record photon weight.

mcmlmain.c, 5K, is the main program.

sample.mci, 1.5K, is an example input file that specifies a particular Monte Carlo run.

sample.mco, 31K, is an example output file generated by MCML.

You may compile the source code with various C compilers. For example, to compile on a UNIX system using the SUN Workstation one enters:

cc -o mcml mcmlio.c mcmlnr. mcmlgo.c mcmlmain.c

which yields an executable program called mcml*.

The output file sample.mco is rather large. It contains all possible data desired from the MCML run. One uses the program CONV to load this sample.mco file and select just the type of output desired. CONV yields small output files suitable for graphing with standard software.