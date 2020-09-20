# Coblife

I implemented Conway's Life in COBOL. Badly. Probably. But it works.

## What is wrong with you?

I don't know.

## How can I find out if you are lying or not?

Why would I lie? Stupid thing to lie about.

But, yeah, it's possible you don't have COBOL lying around on your machine.

I didn't.

A quick `apt install open-cobol` sorted that out for me, running Linux over here.

After that, try `cobc -x coblife.cob -o coblife` and see what happens.

If you are not running Linux, YMMV. At that point, to be fair, it seems reasonable
to suggest that if you want to get a complete randomer's Life implementation in
COBOL running on your machine, you're already at a stage where that kind of thing
shouldn't be a problem in the first place. If it is, I don't really know what to
say to you, other than find a version of COBOL that works locally for you, then
see if you can get my coblife.cob to behave for you.

Numerous weird and wonderful COBOL problems turn out to exist, including the line
length restriction thing and the whatever the hell it is that meant that I couldn't
use my nice iterate over -1 to 1 twice trick I usually like to use when implementing
Conway's Life. It's still there in the code, but commented out, because I was about
yay close from punching a hole through my laptop when I decided that implementing
a brute force neighbour search instead was probably best for my sanity. That worked.

Pull requests welcome if you can figure out how I screwed that up.

Anyway. Now I know why COBOL folk charge so much.

## Really why did you do this

It was about time. My first language was BASIC, and I grew up reading about things
like COBOL, FORTRAN, PASCAL and whatever, but I've never learned any of them.

Seems to me that playing about with the Ur-languages that the ones we use today
grew out of is not a bad idea, as it helps us understand - and be grateful for - a
good deal of the stuff that modern languages do implement, which turn out to be
missing in the older languages.

You know, like proper functions. Or actual variables. Or lines that are allowed
to be longer than 80 characters. Basic shit.

This has been a trip and a half.

## NB

This is very much My First COBOL program, written very quickly after reading
through precisely half of one of the many online COBOL tutorials. The chances
that it is anything other than extremely bad non-idiomatic COBOL are slim.

## Issues (FWIW)

* No editor, you just get the random set of cells
* No way to restart without rerunning the whole thing
* No way to fit arbitrary terminals
* Linenumbers are probably a bad idea and are already a mess
* Paragraphs are in no particular order, code hard to read

## Resources

This was an exercise in learning me a bisl COBOL, so here's some stuff I found
that helped me, and may, if you are still reading this far down, help you too.

### GNU COBOL - https://gnucobol.sourceforge.io/

Your GNU-friendly free COBOL compiler. If you have access to any other COBOL
compiler you are already far more experienced with COBOL than I am.

### GNU COBOL FAQ - https://gnucobol.sourceforge.io/faq/

I should have read at least _some_ of this before starting to write code. In
particular, the section on available tutorials.

### Tutorialspoint COBOL pages - https://www.tutorialspoint.com/cobol/index.htm

This is the kind of tutorial that mixes useful information with stuff that is
so obviously complete rubbish that it becomes an adventure in itself trying to
work out which is which. I gave up with it about halfway through after deciding
I had probably gleaned enough information to write a small and crappy Life
implementation. I have also probably already learned a few things wrong.

### Michael Coughlan's COBOL course - http://www.csis.ul.ie/cobol/course/

This is the one that the GNU COBOL FAQ seems to recommend most highly. Do not be
deceived by the fact that it appears to have been last updated in 2002. As the
GNU COBOL FAQ states: _These pages are over a decade old, and like all things
COBOL, still very relevant at that young of an age._
