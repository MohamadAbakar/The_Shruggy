# Shruggy

**An accessible video game controller for individuals with C4–C5 quadriplegia.**

Shruggy translates shoulder movements into game controller inputs, enabling people who cannot use their arms, hands, or fingers to enjoy modern video games on consoles like the Nintendo Switch, PlayStation, and Xbox, and other electronic devices. 

---

## Motivation

Modern controllers are largely inaccessible to individuals with C4–C5 quadriplegia. Shruggy was developed to close that gap — giving players a comfortable, sustainable, and genuinely convenient experience without requiring any arm, hand, or finger movement.

Unlike some existing assistive technologies, Shruggy deliberately avoids relying on mouth-based input, preserving the player's ability to speak, a critical feature for voice chat and limits potential oral fatigue.

---

## How It Works

Shruggy is a wearable vest with two flex sensors, one at each shoulder, and an electronics housing at the waist.

| Shoulder | Function |
|----------|----------|
| One shoulder | Emulates a joystick or mouse (directional movement) |
| Other shoulder | Selects from 4 distinct button inputs |

This joystick + 4-button layout mirrors the core input scheme found on all major gaming consoles. The combination supports **simultaneous movement and action input**, all driven entirely by shoulder position.

The flex sensors read shoulder positioning, which the onboard microcontroller interprets and translates into standard controller commands sent to the console.

---

## Hardware

- Wearable vest with flex sensors at each shoulder
- Electronics casing mounted at the stomach
- Arduino Uno

**Total build cost: ~$31**

---

## Technical Highlights

- Reads analog flex sensor values to determine shoulder positioning
- Maps shoulder states to joystick axes and button presses
- Proof of concept targets the **Nintendo Switch** via a reprogrammed **ATmega16U2** USB-to-serial microcontroller on the Arduino Uno — a chip not typically meant to be user-programmed — to spoof a recognized HID controller over USB

---

## Design Goals

- ✅ No arm, hand, or finger movement required
- ✅ Mouth and voice left free for communication
- ✅ Comfortable for extended sessions
- ✅ Low-cost and reproducible (~$31 in parts)
- ✅ Compatible with mainstream console/computer input schemes

---

## Future Work

- Expand HID compatibility to fit more intricate controllers (i.e. PlayStation, Xbox, etc)
- Refine sensor calibration for a wider range of users
- Explore wireless transmission
- User testing with individuals with C4–C5 quadriplegia

