# VASM
My personal mirror of the VASM assembler (http://sun.hasenbraten.de/vasm/)

## Compilation Instructions

To compile vasm you first have to choose a Makefile which fits for your host architecture. The following are available:

* Makefile - standard Unix/gcc Makefile
* Makefile.68k - makes AmigaOS 68020 executable with vbcc
* Makefile.Haiku - gcc Makefile which doesn't link libm
* Makefile.MiNT - makes Atari MiNT 68020 executable with vbcc
* Makefile.MOS - makes MorphOS executable with vbcc
* Makefile.OS4 - makes AmigaOS4 executable with vbcc
* Makefile.PUp - makes PowerUp executable with vbcc
* Makefile.TOS - makes Atari TOS 68000 executable with vbcc
* Makefile.WOS - makes WarpOS executable with vbcc
* Makefile.Win32 - makes Windows executable with MS-VSC++
* Makefile.Win32FromLinux - makes Windows executable on Linux

Then select a CPU- and a syntax-module to compile. Do this by defining CPU and SYNTAX for your Makefile, e.g.

```
make CPU=m68k SYNTAX=mot
```

Available CPU modules:
```
CPU=6502
CPU=6800
CPU=arm
CPU=c16x
CPU=jagrisc
CPU=m68k
CPU=ppc
CPU=qnice
CPU=test
CPU=tr3200
CPU=vidcore
CPU=x86
CPU=z80
```

Available Syntax modules:
```
SYNTAX=std
SYNTAX=madmac
SYNTAX=mot
SYNTAX=oldstyle
SYNTAX=test
```

The Makefile will then generate a vasm-binary called: `vasm<CPU>_<SYNTAX>[_<HOST>]`
