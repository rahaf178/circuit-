# Arduino Circuit - 3 LEDs & 3 Pushbuttons

This project is a simple electronic circuit using **Arduino Uno** to control three LEDs with three pushbuttons.

## Components
- **1x Arduino Uno**
- **3x LEDs**
- **3x Pushbuttons**
- Jumper wires
- Resistors for LEDs (optional but recommended)

## How It Works
- When you press any pushbutton, the corresponding LED will turn ON for **3 seconds** and then turn OFF for **3 seconds**.
- If no button is pressed, all LEDs remain OFF.

## Code

// C++ code
void setup()
{
  pinMode(7, INPUT);
  pinMode(4, INPUT);
  pinMode(2, INPUT);
  pinMode(13, OUTPUT);
  pinMode(12, OUTPUT);
  pinMode(8, OUTPUT);
}

void loop()
{
  if (digitalRead(7) == HIGH)
  {
    digitalWrite(13, HIGH);
    delay(3000); 
    digitalWrite(13, LOW);
    delay(3000); 
  }
  else if (digitalRead(4) == HIGH)
  {
    digitalWrite(12, HIGH);
    delay(3000);
    digitalWrite(12, LOW);
    delay(3000);
  }
  else if (digitalRead(2) == HIGH)
  {
    digitalWrite(8, HIGH);
    delay(3000);
    digitalWrite(8, LOW);
    delay(3000);
  }
  else
  {
    digitalWrite(13, LOW);
    digitalWrite(12, LOW);
    digitalWrite(8, LOW);
  }
}
