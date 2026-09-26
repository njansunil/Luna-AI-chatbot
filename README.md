# Luna-AI-chatbot
Building My Own AI Device with ESP32-CAM | Stage 4E  In this video, I’m showcasing Stage 4E of my DIY AI device project.  The project combines an ESP32-CAM, OLED display, Arduino Nano keyboard, and AI communication into a compact experimental device. 
Arduino UART Keyboard code also given in this repo you should download both code from this repo and schematic

STAGE 4E — NANO TO ESP32-CAM

Arduino Nano       ESP32-CAM
--------------------------------
D4 (TX)      ----> GPIO12 (RX)
GND          ----> GND

⚠️ Important: Nano TX is 5 V logic and ESP32 GPIO12 is 3.3 V logic. For a permanent build, use a logic-level converter or resistor divider between Nano D4 and GPIO12.

OLED 0.96" SSD1306     ESP32-CAM
----------------------------------
VCC                 -> 3.3V
GND                 -> GND
SDA                 -> GPIO13
SCL                 -> GPIO14

📷 ESP32-CAM Camera
The AI-Thinker ESP32-CAM camera is connected internally through the board's camera connector, so no external camera wiring is required.

NANO INPUTS

D2  -> ABCD0
D3  -> EFGH1
D5  -> IJKL2
D6  -> MNOP3
D7  -> QRST4
D8  -> UVWX5
D9  -> YZ6789

A0  -> + - * / =
A1  -> Scroll Up
A2  -> Scroll Down
A3  -> Enter / Send
A4  -> Backspace
A5  -> Long press:
       3 sec = Space
       6 sec = Caps toggle

D10 -> Camera button

Normal ASCII -> Typed character

0x08 -> Backspace
0x0D -> Enter / Send
0x11 -> Scroll Up
0x12 -> Scroll Down
0x13 -> Camera

POWER

ESP32-CAM  -> Stable 5V supply
Arduino Nano -> Stable 5V supply
OLED       -> 3.3V
ALL GNDs   -> Common GND

Do not feed 7 V directly into the ESP32-CAM 3.3 V pin. If you're using your battery + buck-converter setup, set the buck output appropriately before connecting it.
