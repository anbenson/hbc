# hbc

hbc is a C compiler that plays the 'Happy Birthday' tune if your code
dereferences NULL. It's undefined behavior, so this is a legitimate thing to do,
even if unwise.

This is a placeholder for the actual source code of hbc. My employer requires
me to go through a releasing process before publicly posting code I write on my
free time since they own the copyright. I don't have time to go through the
releasing process at the moment, but once I do and am approved, I will post the
source code here.

hbc is implemented mostly as a LLVM compiler pass (I had ~24 hours to do this,
so I kind of cheated, okay?). The source code is a collection of files (the LLVM
compiler pass, the code that plays Happy Birthday, the audio file itself) along
with a generator script that inlines everything into a single bash script (that
is self-contained, assuming your machine has LLVM, gcc, libcanberra, and a bunch
of other dubious assumptions).

The output bash script turns out to be less than 100 lines of code (since some
things are inlined into a single line), and I'm allowed to publish that
separately. You can find that
[here](https://gist.github.com/anbenson/79e3599b0e3489c714bbbd21ebbc5c7f), and
hopefully you are able to get it to work on your machine.
