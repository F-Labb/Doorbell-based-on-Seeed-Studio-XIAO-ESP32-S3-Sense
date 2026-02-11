# Doorbell-based-on-Seeed-Studio-XIAO-ESP32-S3-Sense
A custom doorbell project with Home Assistant integration via ESPHome. The device supports video streaming, button LED control, and keypress tracking.

**Features**

• Controller: ESP32-S3 (with Octal PSRAM support for stable video).

• Camera: Supports 800x600 video streaming.

• Indicator: Button LED with breathing effect (pulse) when idle/pressed.

• Sensors: Binary pressure sensor with debounce protection and software timeout.

• Framework: Runs on esp-idf for better network stack performance.

**Description of the logic**

• Visual feedback: When pressing the physical button (press), the LED pulsation effect is automatically activated.

• Timeout: A virtual button with the delayed_off: 300s filter is forwarded to Home Assistant. This is convenient if you want the "Someone is calling" status to remain visible in the interface for a while after being pressed.

• Wi-Fi optimization: LIGHT power save mode is enabled to reduce chip heating without losing connection.
