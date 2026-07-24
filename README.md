# WiFi E-Paper Photo Frame

A fully offline photo frame built with an ESP32 and a 4.26" Waveshare e-paper display (800x480). No internet needed — the device creates its own WiFi hotspot, and any phone can connect and send content straight to the screen.

## Features
- Upload a photo from your phone browser, no app needed
- Type text or paste a link to auto-generate a QR code
- Pick from ready-made office signs (Lab, R&D, Break Room, etc.)
- Run a slideshow of up to 5 photos with a custom timer
- Images are saved to flash memory, so nothing is lost after a restart
- Zero power needed to keep the image on screen once it's drawn (that's the nature of e-paper)

## Built with
- Arduino IDE
- ESP32
- GxEPD2 (e-paper display driver)
- ESPAsyncWebServer (handles the web page and image uploads)
- LittleFS (on-chip storage for saved images)

## How it works
The phone browser turns whatever you choose (photo, text, sign, or slideshow) into a black-and-white image, then sends it to the ESP32 over WiFi. The ESP32 saves it to flash storage and draws it on the e-paper screen.

Built during my R&D internship at MachaDev.
