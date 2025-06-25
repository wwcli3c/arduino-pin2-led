# arduino-pin2-led

This is a basic Arduino sketch that demonstrates how to blink an external LED connected to digital pin 2, while also toggling the built-in LED on the board.

## 🛠️ Hardware Requirements

- Arduino Uno (or compatible board)
- LED
- 220Ω resistor (optional for current limiting)
- Breadboard and jumper wires

## ⚡ Circuit Diagram

- Connect the **positive leg** (anode) of the LED to **pin 2**
- Connect the **negative leg** (cathode) of the LED to **GND** (through a resistor if needed)


-How It Works:

- Sets pin 2 as output in `setup()`
- In the `loop()`, it:
  - Turns pin 2 **HIGH** (LED ON)
  - Waits for 1 second
  - Turns built-in LED (on `LED_BUILTIN`, usually pin 13) **LOW**
  - Waits for 1 second
- Repeats indefinitely

//c++
void setup()
{
  pinMode(2, OUTPUT);
}

void loop()
{
  digitalWrite(2, HIGH);
  delay(1000); // Wait for 1000 millisecond(s)
  digitalWrite(LED_BUILTIN, LOW);
  delay(1000); // Wait for 1000 millisecond(s)
}

