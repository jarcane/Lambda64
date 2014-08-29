Lambda64
========

An 8-bit virtual platform inspired by classic computer and game consoles, powered by Racket

Description
-----------

The Lambda64 is an 8-bit virtual machine, emulating a novel RISC stack-machine architecture provided by MicroMini, as well as roughly period-correct graphics and sound hardware. The aim is to provide an easy-to-use, easy-to-learn, and well documented target platform for retrocomputing and retro-gaming projects.

Lambda64 is also the reference implementation of that virtual machine, developed in Racket, as a demonstration of the power and ease of use of this excellent modern Lisp dialect.


Why?
----

There is considerable interest, especially in gaming circles, for retro and classic computer and console inspired projects at present. Such projects are essentially presented with two options:

1. Target one of the original platforms. This is problematic for a number of reasons, from the difficulty in relearning hardware that is often rife with undocumented, inconsistent, or idiosyncratic behavior, to the potential legal issues arising from trying to distribute such projects in a cross-platform way that's friendly to non-technical users.
2. Develop from scratch on modern platforms and tools. This is the more popular option, however it is itself sometimes unsatisfactory: modern tools are designed to make modern software, and producing authentic results can require quite a bit of effort and reinventing of the wheel. Results are often inconsistent and unrealistic to the original era.

By providing a stable, consistent, and well-documented virtual platform, the Lambda64 VM becomes a real plausible target for authentic results that can run unmodified on any platform with an implementation of the Lambda64 machine.

Racket?
-------

The reference implementation is built on the MicroMini core, a virtual stack machine developed in Racket, a modern descendant of the Scheme family of Lisp dialects. Racket is powerful, well-documented, easy-to-learn, and easy-to-use, and this author believes to be a superior Lisp dialect that combines the power and clarity of the Lisp-1 model with a Python-esque approachability and power without the performance cost.

The MicroMini engine itself is a testament to the power provided by Lisp and Racket: the original CPU core is only 206  lines of code! 

MicroMini
---------

MicroMini is an admittedly unusual choice for a machine of this era, using a minicomputer-inspired RISC stack-machine model rather than the usual register-machine model of the most popular microprocessors of the era, such as the 6502 and 6809. However, there is precedent for such a possible alternate history (see for instance, the Transputer), and as well, the stack machine architecture is quite easy to learn even for a machine-language neophyte, and provides a potentially easier target for some modern programming languages (such as Lisp!).

With only a few minor revisions the toy implementation provided by the MicroMini should prove more than powerful enough for a project of this scope. 

Specifications
--------------

* 8-bit data bus
* 16-bit address bus (64Kib max address page)
* Single 16-byte stack
* 8-bit cycle timer
* 40 x 25 (8x8 font) character text mode
* 320 x 200 graphics mode w/16 colors per pixel
* Sound generator TBD
