# Ratio
Just Intonation VST Synthesizer in Java

Ratio is a just-intonation VST synthesizer built in Java and utilizing jVSTwRapper by Daniel Martin . It takes incoming MIDI notes and maps them to different scales. Left unaltered, MIDI notes sent to a synthesizer will play the 12-tone equal temperament (12-TET) scale, where every note is an equal proportional distance from its neighbor. This scale became popular in the 18th century with the standardization of keyboard design and the rise of modulation as a compositional tool. Prior to this, musicians and composers divided the octave into various numbers of steps and interval distances, ending up with scales ranging from 5 to over 30 notes, unevenly spaced and often based on simple integer ratios.

Ratio offers a choice of six different scales, including 12-TET and 24-TET (also known as the quarter-tone scale.) The other four scales, all of which contain 12 or 24 notes per octave, are based on a fundamental tone multiplied by integer ratios. The 24 note scales start two octaves above and end two octaves below the 12 note scales, but their range can be extended with the Osc1Oct and Osc2Oct parameters.

The Just Intonation (Just) scale is based on the simplest possible fractions. The ratios to the fundamental for each scale degree are: (1) 1/1 (2) 16/15, (3) 9/8--M2, (4) 6/5--m3, (5) 5/4--M3, (6) 4/3--P4, (7) 7/5, (8) 3/2--P5, (9) 8/5--m6, (10) 5/3--M6, (11) 7/4--m7, (12) 15/8.

The Pythagorean (Pythag) scale, in wide use until the advent of equal temperament, is based on multiples of the 3/2 (perfect fifth) interval. The ratios to the fundamental for each scale degree are: (1) 1/1, (2) 256/243, (3) 9/8--M2, (4) 32/27--m3, (5) 81/64--M3, (6) 4/3--P4, (7) 729/512, (8) 3/2--P5, (9) 128/81--m6, (10) 27/16--M6, (11) 16/9--m7, (12) 243/128.

The Aulos scale, in use since the dawn of music, is an undertone scale, which means that the scale tones are produced by dividing rather than multiplying the fundamental by small integers. The ratios to the fundamental for each scale degree are: (1) 1/1, (2) 24/23, (3) 24/22--M2, (4) 24/21--m3, (5) 24/20--M3, (6) 24/19, (7) 24/18--P4, (8) 24/17, (9) 24/16--P5, (10) 24/15--m6, (11) 24/14--M6, (12) 24/13--m7.

The Indian Shruti scale, normally 22 notes per octave but adapted in Ratio to a 24-note scale, is very close to a superimposition of the Pythagorean scale and the Just scale. The ratios to the fundamental for each scale degree are: (1) 1/1, (2) 256/243, (3) 16/15, (4) 10/9, (5) 9/8--M2, (6) 32/27 , (7) 6/5--m3, (8) 11/9, (9) 5/4--M3, (10) 81/64, (11) 4/3--P4, (12) 27/20, (13) 45/32, (14) 729/512, (15) 3/2--P5, (16) 128/81, (17) 8/5--m6, (18) 13/8, (19) 5/3--M6, (20) 27/16, (21) 16/9--m7, (22) 9/5, (23) 15/8, (24) 243/128.

Other than the tuning differences, Ratio is a fairly straightforward subtractive synthesizer, with two oscillators, a Moog-style resonant filter, a pink noise generator, and two LFOs (one unsynced and one tempo-synced.) The two main oscillators are complemented by subharmonic and superharmonic oscillators, adding undertones and overtones, respectively. The fundamental tone, set by the FundKey parameter, can be A440Hz or any of the 12-TET pitches. The KeyMod parameter will remap the scale tones based on the selected interval.

For example, the Just scale with A440Hz as the fundamental will re-orient to a 660Hz fundamental (440Hz * 3/2) if KeyMod is set to P5 (perfect fifth interval.) The exact frequency and scale degree shifts will vary by scale. A major sixth (M6) interval is a 5/3 (10th degree) shift in the Just scale, a 27/16 (10th degree) shift in the Pythagorean scale, a 24/14 (11th degree) shift in the Aulos scale, and a 5/3 (19th degree) shift in the Shruti scale.

Also, if the PulseWd parameter is set to zero, the pulse wave oscillator will become a square wave oscillator--PulseWd applies to both oscillators. 

To install on a Mac, drop the Ratio.vst file into your VST folder.
