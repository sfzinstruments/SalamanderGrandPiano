# Salamander Grand Piano v3

Author: Alexander Holm

## Description

Recorded @ 48khz24bit
16 Velocity layers Sampled in minor thirds from the lowest A.
Hammer noise releases chromatically sampled in onle one layer.
String resonance releases in minor thirds in three layers.
Two AKG c414 disposed in an AB position ~12cm above the strings.

Source: <https://archive.org/details/SalamanderGrandPianoV3>

Remapped by kinwie using sfz format v2 with ARIA extensions in flac format,
combined the Natural and Retuned version into 1 single sfz,
selectable using keyswitch.

## Compatibility Notes

This SFZ Instruments is reconstructed with the heavily use of SFZ specification level 2.0 + ARIA Extensions. With this is mind, this Salamander Grand Piano will only played properly in Plogue sforzando and similar sfz samplers that used ARIA Engine. Trying to play this instrument in other than ARIA-based sfz samplers may cause issues and problems if it doesn't support the opcodes superset used in this sfz instrument. If ARIA-based sfz sampler is not your choice, we advised you to choose a sfz sampler that has similar level of opcodes support for this instrument can be played and sounded as it should.

## Update Log

- Dec 20, 2021 : Optimizing pedal noise as on/off triggered only, to avoid the possibility of multiple-trigger when using continuous sustain pedal type (half-pedaling type).

- Sep 20, 2021 : Fix undampened high notes that "too sustained", by revert back to the use of ampeg_release instead of loop_mode=one_shot. Most noticeable at key F6 to Bb6 (89 - 94). This issue was reported by user james-sounds-crazy. Also simplifying sustain CC by using standard hard-coded MIDI CC number 64 and remove its #define macro.

- Aug 14, 2020 : Optimizing polyphony groups for the release triggered regions.

- Jun 6, 2020 : Added adjustable sample start (offset) from Jeff Learman settings for optional faster response using Flexible velocity layer settings.

## License

<a rel="license" href="http://creativecommons.org/licenses/by/3.0/">
    <img alt="Creative Commons License" style="border-width:0"
        src="https://i.creativecommons.org/l/by/3.0/88x31.png" /></a><br />
This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by/3.0/">
Creative Commons Attribution 3.0 Unported License</a>.
