# 🌈 PWM LED Fader – ESP32 Multi-Color Light Sequence

Smooth multi-color LED fading using PWM on an ESP32. This sketch drives 5 LEDs with a wave-like fading animation using high-frequency PWM for precise brightness control.

---

## 🔌 GPIO Pin Mapping

| LED Color | GPIO Pin | ESP32 Label | Resistor | Notes                       |
|-----------|----------|-------------|----------|-----------------------------|
| Red       | GPIO 2   | G2          | 220Ω     | Anode (+) to GPIO pin       |
| Yellow    | GPIO 4   | G4          | 220Ω     |                             |
| Green     | GPIO 5   | G5          | 220Ω     |                             |
| Blue      | GPIO 15  | G15         | 220Ω     |                             |
| White     | GPIO 18  | G18         | 220Ω     | Can be used for blinking    |

---

## 🛠️ Setup Instructions

1. Place 5 LEDs on a breadboard.
2. Connect each **anode (+)** of the LEDs to the ESP32 GPIO pins through **220Ω resistors**.
3. Connect all **cathodes (–)** of the LEDs to the **GND rail** on the breadboard.
4. Connect the **GND rail** to any **GND pin** on the ESP32.
5. Upload the `PWM_LED_Fader.ino` sketch using Arduino IDE or PlatformIO.
6. Watch your LEDs smoothly fade in and out one after another!

---

## ⚙️ Features

- Smooth fading animation using PWM
- Independent channel control for 5 LEDs
- 8-bit resolution and 50kHz frequency for flicker-free output
- Great introduction to ESP32's `ledcWrite()` and PWM system

---

## 🧠 How It Works

- Each LED is assigned to a separate **PWM channel**.
- LEDs **fade in** from 0 to 255 brightness, then **fade out** back to 0.
- Delay between brightness changes controls fade speed.
- Repeats for each LED in a loop, creating a wave effect.

---

## 📃 License

MIT License — free to use, modify, and share.

---

## 💡 Tips

- Adjust `delay(3)` in the `fadeLED()` function to speed up or slow down fading.
- Try using 12-bit resolution (`resolution = 12`) for even smoother fades (range becomes 0–4095).
- This setup is great for building ambient lights, breathing effects, or notification indicators.

