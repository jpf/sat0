# sat0
The "SAT0" program from Don Knuth's list of "Programs to Read"

This is a repositoy that contains the "untangled" version of Don Knuths WEB program "sat0".

Here is how I generated the files in this repository:


Download the `sat0.w` file:

    wget http://www-cs-faculty.stanford.edu/~uno/programs/sat0.w

Install the cweb suite of programs, this is how I do it on Mac OS X:

    brew install cweb

"Weave" the `.tex` file from the WEB program and convert it to PostScript:

    cweave sat0.w
    tex sat0.tex
    dvips sat0.dvi

(I converted the `.ps` file that `dvips` creates using the Preview.app program on Mac OS X)


Lastly, "tangle" the `.c` file from the WEB program:

    ctangle sat0.w 


Thus, from the single `sat0.w` file, we get the documentation in `sat0.pdf` and the C source code in `sat0.c`
