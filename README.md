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

Audio demo : https://sfzinstruments.github.io/pianos/salamander

## Compatibility Notes

This SFZ Instrument is reconstructed with the heavily use of SFZ specification level 2.0 + ARIA Extensions. With this is mind, this Salamander Grand Piano will only played properly in Plogue sforzando and similar sfz samplers that used ARIA Engine. Trying to play this instrument in other than ARIA-based sfz samplers may cause issues and problems if it doesn't support the opcodes superset used in this sfz instrument. If ARIA-based sfz sampler is not your choice, we advised you to choose a sfz sampler that has similar level of opcodes support for this instrument can be played and sounded as it should.

## Control Details

- String Res : Volume of the string resonance
- Hammer Noise : Volume of the key-release noise
- Pedal Noise : Volume of the pedal noise (on the sustain pedal)
- Sus Pedal : Sustain pedal position (up-down)
- Release : Release time for the sustain layers
- Offset : Sample start for faster touch response
- Veltrack : Dynamic range / velocity to volume response

## Improvements and Features

- This piano has the note-selfmasking sfz native feature and polyphony optimized. This means, when playing a lot of notes (e.g. repetitive, trills or sustain pedal down), the voices count will be handled effectively and lower, which also means less jumping in CPU usage and results in more natural piano sound behavior.

- When not used, lowering the String Res, Hammer Noise and Pedal Noise to 0% also disabling those layers which means free up their polyphony usage and lowering voice count, so lesser CPU and RAM usage.

## Usage Tips

- Salamander Grand Piano sets its default amp_veltrack value at 73%. This mean playing softly (low velocity) will result at higher volume than usual. Setting this veltrack value to achieve a pleasant dynamic range that suit you also depend on your playing style and your keyboard/MIDI controller touch response. Try increase and decrease this "Veltrack" parameter as you play and feel the suitable one for you. To change the default value permanently, find this line in the sfz file : `set_hdcc$VELTRACK=0.73` and change the value to the one that you wanted, range from 0 to 1.

- MIDI CC numbers are assigned at the top of the sfz file with the #define macro. They can be quick and easily changed to your personal favor or to match your MIDI controller device setup. After loading the instrument in sforzando, click the "Open In Text Editor" blue button at the INFO page, the sfz file will open by your default text editor. You will see a list of parameter's defined numbers. Change the number to your preference and then save it (e.g. Ctrl+S in WinOS), the CC numbers are updated to new ones. This is a handy feature in sfz and is a bit similar to MIDI Learn function.

- If you are an advanced user and well understand this SFZ format, you can also modify anything in this sfz instrument to your personal taste, make new presets and settings that suit to your private need. SFZ is an easy-to-learn format and very editable. However, if you use this sfz as your basis to create a new one and want to distribute it, we just ask to explicitly put a note that it's derived from this sfz instrument in this github repository.

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
