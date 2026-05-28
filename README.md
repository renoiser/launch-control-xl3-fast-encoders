# LaunchControlXL3 Fast Encoders

Custom Ableton Live 12 MIDI Remote Script for the Novation Launch Control XL 3.

This variant keeps the stock Ableton `Launch_Control_XL_3` script behavior, but makes the DAW-mode encoders faster by adding `mapping_sensitivity` to the upper and lower encoder elements.

## Current setting

```python
ENCODER_MAPPING_SENSITIVITY = 3.0
```

Lower values are more precise. Higher values are faster.

- `1.0`: stock/default slow speed
- `2.0`: faster and controlled
- `3.0`: good for quick sweeps
- `5.0`: extreme

Floating point values such as `2.5` are allowed.

## Install

1. Close Ableton Live.
2. Copy the `XL3_FastEncoders` folder into Ableton's MIDI Remote Scripts directory.

   macOS:

   ```text
   /Applications/Ableton Live 12 Suite.app/Contents/App-Resources/MIDI Remote Scripts/
   ```

3. Start Ableton Live.
4. Open Preferences > Link, Tempo & MIDI.
5. Select `XL3_FastEncoders` as the Control Surface.
6. Use the Launch Control XL 3 DAW ports:

   ```text
   Input:  LCXL3 1 (DAW Out)
   Output: LCXL3 1 (DAW In)
   ```

## Change the sensitivity

Edit:

```text
XL3_FastEncoders/elements.py
```

Then change:

```python
ENCODER_MAPPING_SENSITIVITY = 3.0
```

After changing it, close Ableton Live and delete:

```text
XL3_FastEncoders/__pycache__
```

Ableton will recompile the script on the next launch.

## Notes

This script is based on the Ableton Live 12.4 `Launch_Control_XL_3` remote script.
