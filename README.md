# KOSMO MULTITOOL POLY CODE
This is a polyphonic code for the Kosmo Multitool by Polykit: https://github.com/polykit/kosmo-multitool

I use this on my personal synth and I wasn't planning on using the quantizer, adsr or multiple modes on there so if you want those in be sure to remove the "//" in the main file. I kept the arpeggiator in because I use that. If you don't want the other modules be sure to remove the files from the director that main.ino is in.

This is an adjustable polyphonic midi to CV converter with 4 cv pitch controls, gate, pitchbend, a forward cycle, a backward cycle, and a random cycle. The poly modes are MONO, DUO, POLY, UNI 2 and UNI 4. Pitch bend is converted from midi and added or subtracted directly from all the cv pitches. Adjustable by 1, 2, 3, 4, 5, 7, 12 and 24 semitones.

This is still a work in progress and feel free to improve upon this code. I want to add a uni/poly mode that plays all the voices at once and changes the polyphony based on the notes played (IE, one note plays uni 4, 2 plays uni 2, 3 plays uni 2 on bass and the other two are separate and then 4 is regular poly) There is also a bug that some pitch bends will change the note data causing the notes to latch permanantly and It's my first problem to tackle. (Play c4 and pitchbend is all the way up, some midi devices I've tested just send a d4 or eb4 which can open up the gates for that note instead of c4 and a pitchbend value of 127) For the most part this works and I use it more than my midimuso unit but that one definitely has it's strengths. My plan after this is to move this into its own unit POSSIBLY and programmable midi cc to cv sort of how the midimuso can handle so many cv values as well as velocity and aftertouch. This is based on a development board with only 4 cv gate and 4 cvs out and 4 gate 4 cv in respectively.

*Also be sure to take a peek towards the bottom of main.ino to see the changes with how voices are allocated and removed as well as pitchbend and how the robin modes are calculated. as well as the midi.h library to see the selectable options
