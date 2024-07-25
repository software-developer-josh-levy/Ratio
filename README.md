# Ratio Manual
Just Intonation VST Synthesizer in Java

Ratio is a just intonation VST synthesizer built in Java and utilizing jVSTwRapper. It takes incoming MIDI notes and maps them to different tunings. Left unaltered, MIDI notes sent to a synthesizer will play the 12-tone equal temperament (12-TET) tuning, where every note is an equally proportionate distance away from its neighbor. This tuning became popular in the 18th century with the standardization of keyboard design and the rise of modulation as a compositional tool. Prior to this, musicians and composers divided the octave into various numbers of steps and interval distances, ending up with tunings ranging from 5 to over 30 notes, unevenly spaced and often based on simple integer ratios.

Ratio offers a choice of six different tunings, including 12-TET and 24-TET (also known as quarter-tone tuning.) The other four tunings, all of which contain 12 or 24 notes per octave, are based on a fundamental tone multiplied by small fractions. The 24-note tunings start two octaves below and end two octaves above the 12-note tunings, but their range can be extended with the Osc1Oct and Osc2Oct parameters.

The Just Intonation (Just) tuning is based on the simplest possible fractions. The ratios to the fundamental tone for each scale degree are: (1) 1/1—fundamental, (2) 16/15—m2, (3) 9/8—M2, (4) 6/5—m3, (5) 5/4—M3, (6) 4/3—P4, (7) 7/5—tritone, (8) 3/2—P5, (9) 8/5—m6, (10) 5/3—M6, (11) 7/4—m7,  and (12) 15/8—M7.

The Pythagorean (Pythag) tuning, in wide use until the advent of equal temperament, is based on multiples of the 3/2 (perfect fifth) interval. The Aulos tuning is an undertone tuning, which means that the constituent tones are produced by dividing rather than multiplying the fundamental tone by small integers. The Shruti tuning, normally 22 notes per octave but adapted in Ratio to 24 notes, is very close to a superimposition of the Just and Pythag tunings.

Other than the tuning differences, Ratio is a fairly straightforward subtractive synthesizer. It has two primary oscillators, a Moog-style resonant filter, a pink noise generator, and two LFOs (one unsynced and one tempo-synced.) The two main oscillators are complemented by subharmonic and superharmonic oscillators, adding undertones and overtones, respectively. The fundamental tone, set by the FundKey parameter, can be A(440Hz) or any of the 12-TET pitches.

The KeyMod parameter will remap the tones based on the selected interval. For example, Just tuning with 440Hz as the fundamental will re-orient to a 660Hz fundamental if KeyMod is set to P5 (3/2 interval.) The exact frequency and scale degree shifts will vary by tuning.
Also, if the PulseWd parameter is set to zero, the pulse wave oscillator will become a square wave oscillator. PulseWd applies to both oscillators.

Java must be installed on your computer to run Ratio. To install Ratio on a Mac, unzip "Ratio for Mac" and drop "Ratio.vst" into your VST folder. For Windows, unzip "Ratio for Windows" and drop the entire "jVSTwRapper-Release-1.0beta" folder into your VST folder. In your DAW, select and open the "jVSTwRapper-1.0beta" dll file. If your DAW cannot find Java, you can alter the "CustomJVMLocation" setting in the "jVSTwRapper-1.0beta" text file to reflect the path to your Java installation.
