# ssd1306-esp32-text

This is a combination of the [SSD1306 library text-i2c example](https://github.com/jamwaffles/ssd1306/blob/master/examples/text_i2c.rs) with the I2C examples from the [esp-idf-hal](https://github.com/esp-rs/esp-idf-hal/blob/master/examples/i2c_ssd1306.rs) library.   

## Steps

This was written for an unidentified ESP32 dev board, 30 pins with an ESP-WROOM-32 module.

It is driving a 128x32 OLED screen of unknown provenance driven by an SSD1306 driver chip.

1. Follow [The Rust on ESP Book](https://esp-rs.github.io/book/) to the point of getting the onboard LED to blink
2. Connect the screen SDA and SCL to the dev board on two output-capable pins e.g. 22, 23
3. Generate new project: 
    cargo generate esp-rs/esp-idf-template cargo  
4. copy contents of `main.rs` from this project
5. `cargo add` the missing modules:
 - `embedded_graphics`
 - `esp_idf_hal`
 - `anyhow`
 - `ssd1306`
6. `cargo run` to compile and upload to the ESP32

