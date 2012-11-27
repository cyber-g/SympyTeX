This is the SympyTeX package. It allows you to embed code, results of
computations, and (sometimes!) plots from the Matplotlib software suite
(http://www.sympy.org) into LaTeX documents.

====================================================================

##USING THE PACKAGE

To use SympyTeX, you need the files
  sympytex.sty
  sympytex.py
If those haven't been extracted from the .dtx file, you'll need  build
the package (see below)

You also need to have installed the Sympy (Symbolic Python) package

    aptitude install python-sympy


====================================================================

##BUILDING THE PACKAGE

To build the SympyTeX package you will need to install some extra LaTeX
packages (makecmds.sty)

    aptitude install texlive-latex-extra

Then do:

  0. Run `latex sympytexpackage.ins'

If a PDF file of the documentation wasn't included with this
distribution of SympyTeX, you will need to build the documentation
yourself. To do that:

  1. Run `latex sympytexpackage.dtx'
  2. Run `python sympytexpackage.sympy'
  3. Run the indexing commands that the .ins file told you about.
  4. Run `latex sympytexpackage.dtx' again.

You can skip step 3 if you don't care about the index. You will need the
pgf and tikz packages installed to typeset the figures.

The file example.tex has, as you likely guessed, a bunch of examples
showing you how this package works.

###The easy way

Use the provided Makefile

    make 
    make test

This will build the SympyTeX package, and also create a sample document.

##CREDITS

This works builds on a lot of work by others; in particular the work of
Dan Drake <ddrake@member.ams.org> who created the sagetex package from which
this is shamelessly copied see the "Credits" section
of the documentation for credits. The source code may be modified and
distributed under the terms of the GPL, v2 or later; the documentation
may be modified and distributed under a Creative Commons Attribution -
Noncommercial - Share Alike 3.0 License. See the "Copying and licenses"
section of the documentation.

Please let me know if you find any bugs or have any ideas for
improvement!

- Tim Molteno <tim@physics.otago.ac.nz>
