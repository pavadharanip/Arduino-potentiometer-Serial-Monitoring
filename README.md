## **📌 Project Overview**

This project demonstrates how to interface a potentiometer with an Arduino UNO and read its analog values using the Serial Monitor. The potentiometer acts as a variable resistor. By rotating its knob, the resistance changes, which changes the voltage supplied to the Arduino's analog input pin. The Arduino reads this voltage and displays the corresponding values on the Serial Monitor using an Arduino C/C++ program.

## **🎯 Objectives**

- To interface a potentiometer with Arduino UNO.
- To understand analog input and output.
- To read changing voltage values using the analog input pin.
- To display potentiometer readings in the Serial Monitor.
- To understand the `analogRead()` and `Serial.println()` functions.

## **🧰 Components Required**

| Component | Quantity |
|---|---:|
| Arduino UNO | 1 |
| Potentiometer (10kΩ recommended) | 1 |
| Breadboard | 1 |
| Jumper wires | 3 |
| USB cable | 1 |

## **🔌 Circuit Connections**

| Potentiometer Pin | Arduino UNO Pin |
|---|---|
| First outer pin | 5V |
| Middle pin (wiper) | A0 |
| Second outer pin | GND |

## **💻 Arduino Source Code**

The Arduino program reads the analog value from the potentiometer and displays it on the Serial Monitor.

```cpp
int potPin = A0;
int potValue = 0;

void setup() {
  Serial.begin(9600);
}

void loop() {
  potValue = analogRead(potPin);
  Serial.println(potValue);
  delay(500);
}
```

## **⚙️ Working Principle**

1. The potentiometer is connected to the 5V, GND, and A0 pins of the Arduino UNO.
2. When the potentiometer knob is rotated, its output voltage changes.
3. The Arduino reads the voltage through the analog pin A0.
4. The `analogRead()` function converts the voltage into a digital value.
5. The `Serial.println()` function displays the reading on the Serial Monitor.
6. The displayed value changes according to the rotation of the potentiometer.

## **📊 Expected Output**

The Serial Monitor displays values ranging from **0 to 1023**.

- At one end of the potentiometer: approximately 0.
- At the middle position: approximately 512.
- At the other end: approximately 1023.

<Note>Actual readings may vary slightly depending on the potentiometer position and supply voltage.</Note>

## **📚 Concepts Learned**

- Arduino UNO programming
- Analog input interfacing
- Potentiometer working principle
- ADC (Analog-to-Digital Conversion)
- `analogRead()` function
- Serial communication
- `Serial.begin()` and `Serial.println()` functions

## **🚀 Future Improvements**

- Display the potentiometer value on an LCD.
- Control LED brightness using the potentiometer.
- Control motor speed based on potentiometer readings.
- Convert analog readings into voltage values.

## **🏁 Conclusion**

This project demonstrates how to interface a potentiometer with an Arduino UNO and monitor changing analog values through the Serial Monitor. It provides practical knowledge of analog input, ADC conversion, and serial communication.

## **🛠️ Technologies Used**

- Arduino UNO
- Arduino IDE
- Embedded C/C++
- Serial Monitor
- Basic electronic components
