# FOV Calculator Notes

Reference notes on field-of-view (FOV) math for FPS games — horizontal/vertical conversion, aspect ratio scaling, and how different game engines handle FOV settings.

## Why FOV conversion matters

Games report FOV differently — some use horizontal FOV, others vertical, and the "same" number can look completely different depending on your aspect ratio or monitor setup. Converting between them requires trigonometry that most in-game settings menus don't explain.

## Core formulas

**Horizontal to Vertical FOV:**
vFOV = 2 * atan(tan(hFOV / 2) / aspectRatio)

**Vertical to Horizontal FOV:**
hFOV = 2 * atan(tan(vFOV / 2) * aspectRatio)

Where aspectRatio = width / height of your display.

## Tool

Built a free calculator that handles these conversions automatically, including aspect ratio adjustments across ultrawide and multi-monitor setups:

🔗 [FOV Calculator Pro](https://fovcalculatorpro.com)

## Notes

- Aspect ratio compounds FOV differences — the same numeric FOV can feel narrower or wider depending on your screen ratio.
- Some engines (Source, Unreal) default to horizontal FOV; others (Unity) commonly use vertical.
- Competitive players often adjust FOV for a tradeoff between situational awareness and target size/precision.
