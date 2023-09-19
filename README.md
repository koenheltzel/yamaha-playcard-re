## Reverse engineering the Yamaha Playcard data format - *an attempt*

Recently I acquired a nice sample Yamaha PC-100, which came with 17 playcards. I was already familiar with the Edward D-tech website and the results of the work he did on digitizing the playcards.
This project is based on Edward D-tech's binaries; thanks Edward (& Jayson Smith) for your work!

Checking out some of the playcards, this seems to be the information that can be present on the playcards:  
- Voice type
- "Obbligato" voice type
- Melody
- Obbligato melody
- Chords (4 types, possibly at quarter note precision, haven't seen faster)
- Breaks & continuations in the accompaniment (twice in Killing me softly).
- Drum Fill-in triggers
- Drum muted sections (while the rest of the accompaniment is playing, for example intro of Singing In The Rain)
- Rhythm is sometimes switched between "normal" and "variation".
- Phrase numbers.

Other observations
- Melodies note durations: 16ths, Triplets, 8ths, swung 8ths, and all combinations upwards to any length.
- The Obbligato melody seems to have the same possibilities as the melody. It reacts to the auto bass chord volume.
- The lamps seem to only be on for 2/3rds of the note duration. Is this specified in the playcard data or is this automatically done by the keyboard based on the melody note durations?
- Are repeats written out in the data or somehow specified to save space?
- Sometimes there are chord changes that are not on the sheet music (during last 4 rest bars of Take The A Train).
- Sometimes quarter notes seem cut off (accented), wonder if this is stored as 8th note or if it is cut off otherwise.
- Music sometimes starts with pickup notes (anacrusis) (for example Aloha Oe, Cielito Lindo).
