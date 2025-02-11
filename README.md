Bash Course
===========

Become proficient at using the terminal and creating bash scripts.

High-level Overview
-------------------

(for dave - not for advertising)

### What it is

A long video, broken into chapters, that will live on YouTube for free.  Any
supplemental material for it will live on GitHub in a repo specific to this
course (probably this repo lol).

Example: 6 hour video total, 20 minute sections = 18 chapters
 - upload as 1 big video
 - also upload as 18 smaller videos in a playlist

### Who it's for

The absolute beginner and the person who wants to look inside bash.c - and
everyone in between.

0-100%: from absolute beginner to proficient and comfortable on a CLI only
interface.

100%+: dig into the source code, look at how things are implemented, complex
data structures in bash - basically how to think of bash as a programming
language more than a scripting language.

0-100% = 85-90% of the course
100%+ = remaining 10-15% of the course - think of it as DLC

Similar video games with 101% completion.  0-100% will get you all the knowledge
to feel proficient and be done.  Everything beyond that is Bonus/DLC/For those
that want a REAL challenge.

### What you'll learn

What a terminal is, how it interacts with your system, and how you can see that
through finder/explorer/file manager/etc. (show the CLI interacting with GUI).

What a shell is (fundamentally a REPL) and how we can interact with it via
commands (external and builtin).

Basic filesystem manipulation commands and visual (GUI) realtime representation
of the work being done. (create, delete, list files - maybe even convert a webp
to jpg).

Basic task automations with scripts - how to take a series of commands and run
them all at once.

Complex task automations with scripts - introduce conditional branching, string
manipulation.

Finally, feel proficient in a CLI environment - be able to edit files (nano,
vim) and rename files in batches. (example mismatch of .jpg and .JPG files -
normalize them).

### What you need

A computer with a terminal emulator:
- Mac with terminal.app (show a little iterm and bash)
- Linux with a terminal
- Windows with WSL (figure out how to help people with this)

A virtualized instance of Linux - maybe show how the user can install vbox to
follow along at home and have the same environment that i have.

No real prior knowledge - try to start from the ground up.

Course Implementation
---------------------

A multi-hour video containing facecam and desktop footage.  Recorded on the
latest (at the time) Ubuntu Desktop ISO.  Virtualized or hardware - it doesn't
matter.

Spend some time explaining how to setup your own test environment - but leave it
mostly up to the watcher to figure out (this will be in the course itself).

Course Outline
--------------

Course
 - Chapters (individual video)
   - Sections (parts of a video)

Rough Estimates
Course ~ 6 hours
Chapter ~ 20 minutes
Num Chapters ~ 18 chapters total

(not even really a chapter - this is just the beginning of the youtube video)
- Why use the terminal? (shotgun this information)
  - (SELL THE WATCHER ON WHY THIS IS COOL)
  - Photographer? Convert folder full of HEIC to jpg
  - Normal Person who's not a photographer? convert folder full of webp
  - Designer? Convert PSD file to PDF
  - Web Designer? Resize image files and reduce quality for thumbnails
  - Not a designer? stitch pdf files together
  - Still stuck in the early 2000's (cuz i am), convert FLAC files to mp3 and
    rename them based on tags
  - None of the above? Rename files based on CTIME
  - AND YOU KNOW WHAT ELSE? renaming files is barely 1% of what the terminal can
    do for you lmao
  - Backup your data to other machines or drives (rsync a folder to a
    thumbdrive)
  - filter CSV data
  - Collection of texts? search for file contents
  - Author? Get a word-frequency count of your works
  - cowsay? draw a cow
  - fortune command
  - `sl` train
  - turn on and off a wifi lightbulb
  - star wars ascii

- What is a terminal?
  - Talk about 1970s computers
  - Terminal emulators for modern PCs
  - Basic text rendering on a monospace font
  - 80x24, ASCII, vt100s
  - Why the were useful (no gui) and why they are still useful (no gui) today
  - Shell runs in the terminal (segue into next chapter)

- What is a shell?
  - Basic input / output
  - REPL and simple iteration loop (state machine, maybe)
  - Managing command execution and optionally displaying to the above terminal
  - No output is good - error loudly
  - Bash is a shell, just like bourne/csh/fish/powershell/nushell/ksh/etc.
  - Recap: shell runs in the terminal

- Getting up and running
  - Explain the environment (ubuntu desktop)
  - Go over how to replicate it
    - Use a vbox VM
    - Use ubuntu on your actual machine
    - Just follow along (there will be homework I encourage you to do)
    - If you don't have linux you can still get something out of this - but your
      experience may be limited
  - Open the terminal and run `echo hello world`

- Basic Command Execution
  - `echo hello world`
  - open folder to home directory, run `ls`
  - `mkdir bash-course`, see it show up
  - `cd bash-course`, also open it in file explorer (everything mirrored)
  - `touch lesson.txt`
  - `cat lesson.txt`
  - (edit lesson.txt with gui)
  - `cat lesson.txt`
  - `echo hi > lesson.txt`, `cat lesson.txt`, `ls`, `touch lesson.txt`
  - `mv lesson.txt new.txt`
  - `rm new.txt`, `ls`, `rm new.txt` (THERE IS NO RECYCLE BIN)
  - rm is scary, try `rm -i`
  - we know how to create directories, change dirs, rename files, and remove
  files
  - homework: basic filesystem manipulation

- Basic Command Execution (cont)
  - also, it can be easy to get lost, here's `pwd`
  - `touch lesson-1.txt`
  - edit
  - `cp lesson-1.txt lesson-2.txt`
  - cp vs mv
  - `rm lesson*.txt` (gloss over globbing)
  - we don't have a trash, we could implement it... and that's the lesson about
    the shell and linux and unix in general - you always have the option to make
    your own lol.
  - `rm -i` seems useful now, can we make it the default?
  - `man rm`
  - `alias rm='rm -i'`
  - `touch .lesson.txt`
  - `ls`
  - homework: list the hidden file what - argument/flag can i give `ls` to see
    hidden files?

- Search inside files (grep)

use unix.daveeddy.com as a loose guide
/usr/share/dict/words - check if this exists
gutenberg free books - wget some and grep them
head/tail
bg/fg

ansi/ascii/control characters (ex: cat /bin/my-binary-file)

Metadata
--------

Title: Bash and Linux Terminal THE COMPLETE COURSE - From beginner to advanced
bash, shell scripting, and command line wizardry.

NOT SCARY - don't be intimidated!

Rated E for everyone
