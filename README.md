# Potentiometer Reading with Arduino 🎛️

A simple Arduino UNO project that reads the analog value of a potentiometer and prints it to the Serial Monitor.

## How It Works

The potentiometer acts as a variable voltage divider. As you turn the knob, the voltage on the middle pin (wiper) changes between 0V and 5V. The Arduino reads this voltage on an analog pin and converts it into a number between 0 and 1023.

## Components Used

- Arduino UNO
- Breadboard
- 1x Potentiometer
- Jumper wires

## Wiring

| Potentiometer Pin | Arduino Pin |
|---|---|
| Outer pin 1 | 5V |
| Middle pin (wiper) | A0 |
| Outer pin 2 | GND |

> **Note:** The two outer pins connect to 5V and GND (order doesn't matter), and the middle pin connects to an analog input pin. On a breadboard, each leg of the potentiometer just needs to sit in its own row — the rows don't have to be consecutive.

## Code

```cpp
#define potpin A0

int deger = 0;

void setup() {
  Serial.begin(9600);
  Serial.println("Pot Değer Okuma");
}

void loop() {
  deger = analogRead(potpin);
  Serial.println(deger);
  delay(300);
}
```

## Circuit Setup

<img width="492" height="272" alt="Screenshot 2026-07-02 at 13 07 41" src="https://github.com/user-attachments/assets/a2f42472-d0c1-4757-b6fb-ce9a7bcf597d" />

** note: you can open Serial Monitor with ```Ctrl + Shift + M``` or ```Command + Shift + M```

## License

This project is shared for educational purposes — feel free to use and modify it as you like.
