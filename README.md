# AbstractOS-infoOS-juliaOS-MagicOS-HumanOS
next gen OS: speak to your OS and it will do ... anything

# UI
human user talks to OS
OS shows information visually or with audio

# Basics
ML learns from the OS API documentation (written in human language) how to create code based on human prompt. The newly created code (incl. its human language documentation) is added to the OS API. This allows a bootstrapping of an OS that can do "anything" just by talking to it.

Eventually, the OS has enough complex code defined and the ML is complex enough to let the user created on-the-spot-made-up apps for the user.
(Magic)

# Example
"device, i would like to play a game where an object flies that this and that and that else happens and it should be this" ... <screen shows game>

# Interaction
each use<->OS interaction is a function call on some input info and access to output info. arbitrary functions on arbitrary data. functions can panic which causes no change to data (does this mean no pointers allowed?).

# julia
the OS runs inside a julia runtime giving the OS Turing complete power over a computer capable to doing arbitrary-precision and high-complexity calculations. the base language of the OS is julia itself, since julia can parse julia code from string format into object trees or even LLVM code, which allows runtime manipulation. 

# Apps
an app only provides an API. what used to be a menu on the top (etc. 'File','Edit',...) is each a command of the API of the app.

e.g. a image viewer app had a button called 'Left Rotate'; instead of clicking on that button, the user simply says "rotate it left" and the ML creates code learned from the documentation of all the available code in the OS including the apps and the ML writes code to call the app's rotate_left API method which outputs information respresenting the rotated image, which can be decoding as an image on a socket (e.g. screen)

all API methods should be descriptive in human language

# Code
initially, the OS can do what julia can do. the user then combines code to create more useful code. e.g. the user asks the OS to write code to show a website. this code combines downloading over HTTPS then rendering HTML. the OS writes this function including documentation making this function part of the language that the OS understands.

# ML Visuals
the output of the code executed on behalf of the command of the user can be interpreted by an ML to create visuals thereof. this part sometimes needs exact info trust and no hallucinations. e.g. there can be code that would show a text exactly as any famous text editor would show it, but all the context around it (usually the window frames, icons and such) would be generated by the ML, uniquely every time. 
the user asked to see some text and got to see it albeit visually slightly different each time.

# Filesystem
a tag based file system. e.g. user driven "tag these as 'holidays in the mountains'" and code will be written to do so. other tags can be derived from ML.

# Logging
each interaction with the OS is the OS running some with some input info and writting the response somewhere. each interaction with the OS is a function instantiation. each such function call can be (representably) logged allowing for perfect replay of the device.

# Permissions
perhaps later; for now, such an OS can be run inside each other! each OS instance can be a VM

# ML to write code
e.g. a Transformer learns how to code the OS learning on julia base all added code

# more ML
ML (e.g. Whisper) converts audio to text
ML (e.g. GAN) to create visual or audio output

# use cases
any device used by humans

# Humans
literally for humans: the OS that takes human input and gives arbitrarily complex output

# Sharing
simple sharing of arbitrary information

# VM
each VM is a powerful virtual computer and can contain further VMs inside without limit

# Reputation
for sharing of info (to be run as code or not)

# info
info contains info

# Typing
it is the clean julia typing system that allows for the flexible decoding of arbitrary info

# API
julia
run(code::Code<:Info, input::Info) :: Info

# MVP
e.g.
bmp on filesystem -> ask OS to show file (as a bmp, specified or set by default by this info)
OS cannot (pure julia has no show_bmp function)
human guides OS: open file byte by byte, extra RBP from each byte, draw a canvas with pixel of RGB, show canvas
OS learns via documentation of above function
ask OS to show file and it does
ask OS to show folder full of bmp files with 10 seconds apart -> OS writes correct code
OS knows how to use a loop to run the folder task once it knows how to do a single file
OS and human together (as cyborg) created a bmp caroussel on a system that could not within a minute

# stream
https://youtube.com/live/Gatf8ltrMKQ
