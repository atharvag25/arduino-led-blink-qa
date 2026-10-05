# arduino-led-blink-qa
# Arduino LED Blink with QA Documentation

A simple embedded project that blinks an LED on pin 13 of an Arduino Uno, documented and quality-checked using GitHub Issues.

## Components
- Arduino Uno
- 1 x LED (any color)
- 1 x 220 ohm resistor (220-330 ohm is acceptable)
- Jumper wires
- USB cable

## Wiring
| From | To |
|---|---|
| Arduino pin 13 | One end of the 220 ohm resistor |
| Other end of resistor | LED anode (long leg) |
| LED cathode (short leg) | Arduino GND |

The onboard LED on pin 13 also blinks without any external wiring.

## Upload Steps
1. Install the Arduino IDE.
2. Open `blink.ino`.
3. Select **Tools > Board > Arduino Uno** and the correct COM port.
4. Click **Upload**.
5. Open the Serial Monitor at 9600 baud.

## Expected Output
- The LED turns ON for 1 second and OFF for 1 second, repeatedly.
- The Serial Monitor prints `LED blink started`, then alternates `LED ON` and `LED OFF`.

## Test Result
| Test | Expected | Observed | Status |
|---|---|---|---|
| LED blinks at 1 s interval | ON/OFF every 1 s | ON/OFF every 1 s | Pass |
| Serial output at 9600 baud | Status messages printed | Messages printed | Pass |
| No resistor warning documented | Resistor value in README | Present | Pass |

## Version History
- v1: Basic blink using delay() and hard-coded values.
- v2: Named constants, non-blocking millis() timer, serial debug output, full documentation.
