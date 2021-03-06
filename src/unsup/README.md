# READ-ME FILE for the UNSUPPORTED PROGRAM DIRECTORY
```
****************************** DISCLAIMER: *******************************
     THE AUTHOR OF THE PROGRAMS BELIEVE THEY ARE WORKING PROPERLY AS
   REPORTED IN THEIR SELF-DOCUMENTATION. NEVERTHELESS, THE PROGRAMS ARE
   PROVIDED AS THEY ARE AND NO WARRANTIES ARE DONE WHATSOEVER ON THEIR
  CORRECT WORKING. THE AUTHORS CAN NOT BE LIABLE FOR ANY LOSS OR DAMAGE
  INCURRED FROM THE USAGE OF THESE TOOLS. SEE OTHER RESTRICTIONS IN THE
    IUT-T SOFTWARE TOOL LIBRARY TERMS AND CONDITIONS, AS IN ITU-T
 RECOMMENDATION G.191, REPRODUCED IN PART IN THE MAIN DIRECTORY OF THIS
       DISTRIBUTION (SEE ../LICENSE.md)
**************************************************************************
```

Use them - report any bugs to <simao.campos@labs.comsat.com>

## Source code
```
asc2bin.c:  converts decimal or hex ASCII data into short/long/float or
            double binary numbers. Input data must be one number per line.

astrip.c:   strips off a segment of a file. Can operate on block or
            sample-based parameters and can apply windowing to the
            borders of the extracted segment. Tested in Unix/MSDOS

bin2asc.c:  converts short/long/float or double binary numbers into
            octal, decimal or hex ASCII numbers, printing one per line.

compfile.c  compare word-wise binary files. For VMS/Unix/MSDOS.

dumpfile.c  dump a binary file. For VMS/Unix/MSDOS.

chr2sh.c:   convert char-oriented files to short-oriented (16-bit words)
            files by padding the upper byte of each word of the output
            file with zeros.

endian.c:   program that verifies whether the current platform is big or
            little endian (i.e. high-byte first or low-byte first).

fdelay.c:   flexible program to introduce delay into a file. Delay can be
            specified in value and length, or can be taken from a
            user-specified file.

g728-vt:    a directory with software tools for use with the G.728 floating
            point verification package. Not all tools are functional;
            preserved here for future reference.

getcrc32.c: 32-bit CRC calculation function and program (depending on how
            it is compiled). Uses the same polynomial as ZIP. Checked for
            portability across a number of platforms. Makefile compiles it
            into an executable called crc.

measure.c:  measure statistics/CRC for a bunch of files. For VMS/Unix/MSDOS.

oper.c:     implement arithmetic operation on two files: add, subtract,
            multiply or divide two files applying scaling factors (linear
            or dB), and adding a DC level.

sb.c        swap bytes for word-oriented files. For VMS/Unix/MSDOS.

sh2chr.c:   convert short-oriented (16-bit words) files to char-oriented
            files by ignoring the upper byte of each word of the input file.

sine.c      generate a sinewave file for a given speco of AC/DC/phase/
            frequency/sampling frequency values. For VMS/Unix/MSDOS.

sub-add.c   subtract/add files (depending on the compilation, see
            makefiles). For VMS/Unix/MSDOS.

xdecode.c   uuencode compatible with auto-break/sequencing for long files
            and CRC calculation for error detection. Not functional under
            MSDOS 6.22.

xencode.c   uudecode compatible with auto-break/sequencing for long files
            and CRC calculation for error detection. Not functional under
            MSDOS 6.22.
```

## Scripts
```
rm.bat  fake deletion utility that tries to emulate the basic
        functionality of the Unix command rm, that deletes multiple
        files specified in the command line. Should be put in the
        path, unless you already have a version of rm.

swapover.bat    Batch/Bourne Shell scripts to perform the byte-swap of
swapover.sh     one or more files in a directory using the utility sb.c
                with the option -over (overwrite)
```

## Makefiles
```
makefile.tcc    for Borland [bt]cc C/C++ compiler
makefile.cl     for MS Visual C compiler (cl)
makefile.djc    for MSDOS djc port of gcc
makefile.unx    for Unix make
```

## Test files
```
tstunsup.zip:
   cf:
     3200    cftest1.dat
     3200    cftest2.dat
     3200    cftest3.dat
      186    delay-15.ref
      186    delay-a.ref
      214    delay-u.ref
      186    delaydft.ref
      200    delayfil.ref

   sb:
      100    bigend.src
      100    litend.src

   xencode and xdecode:
     9182    voice.ori
     8705    voice.uue
     2093    printme.eps
     3795    printme.uue
     5368    voice01.uue
```

[Need to have unzip/pkunzip/Winzip installed to extract.]

----
Good luck,
<simao@ctd.comsat.com> 17.May.2000
