# G-Code Dictionary
#note

| Code | Meaning                                            |
| ---- | -------------------------------------------------- |
| A    | Rotation about X-axis                              |
| B    | Rotation about Y-axis                              |
| C    | Rotation about Z-axis                              |
| D    | Cutter diameter compensation (CDC) offset address. |
| F    | Feed rate.                                         |
| G    | G-Code (Preparatory code)                          |
| H    | Tool length offset (TLO)                           |
| I    | Arc center X-vector, also used in drill cycles.    |
| J    | Arc center Y-vector, also used in drill cycles.    |
| K    | Arc center Z-vector, also used in drill cycles.    |
| M    | M-code (miscellaneous)                             |
| N    | Block number                                       |
| O    | Program number (operation)                         |
| P    | Dwell time                                         |
| Q    | Used in drill cycles                               |
| R    | Arc radius, also used in drill cycles              |
| S    | Spindle speed in RPM                               |
| T    | Tool number for ATC                                |

**For example...**

`G01 T01 M03 S500 F20.0 X1.000 Y1.000`

This means:
- `G01` - Perform a linear move
- `T01` - Use Tool 1
- `M03`- Turn the spindle on
- `S500` - Set a spindle speed of 500 RPM
- `F20.0` - Set a feed rate of 20 IPM
- `X1/Y1` - Move to these coordinates (need the decimal point!)

Another example is `M06T13`:
- Z goes all the way up to the ATC, and orients the spindle
- Tool carousel moves into spindle position
- Spindle un-chucks tool
- Carousel rotates to location 13.
- Spindle moves down over new tool
- Spindle clamps new tool
- Carousel moves to storage location