# Quick Reference

## Chip to Chip Connections

#### Serial Connection
| uLisp          | Chip   | Pin  | Function            |
|----------------|--------|------|---------------------|
| `:to-rp2040`   | ESP32  | GP19 | UART Tx to RP2040   |
| `:from-rp2040` | ESP32  | GP22 | UART Rx from RP2040 |
| `:to-esp32`    | RP2040 | GP1  | UART Tx to ESP32    |
| `:from-esp32`  | RP2040 | GP0  | UART Rx from ESP32  |

#### SWD Connection
| uLisp           | ESP32 | RP2040    | Function                                      |
|-----------------|-------|-----------|-----------------------------------------------|
| `:swd-io`       | GP2   | SWDIO     | RP2040 SWD                                    |
| `:swd-clk`      | GP4   | SWCLK     | RP2040 SWD                                    |
| `:swd-use`      | GP5   | n/a       | Set high to use, set low to use external SWD  |
| `:reset-rp2040` | GP23  | Reset pin | Reset RP2040 by setting low then setting high |

## On-board LED Pins

| uLisp         | Chip   | Led    | Pin  |
|---------------|--------|--------|------|
| `:green-led`  | RP2040 | Green  | GP25 |
| `:yellow-led` | ESP32  | Yellow | GP33 |
| `:blue-led`   | ESP32  | Blue   | GP32 |

## ESP32 Pinout (UEXT)
| uLisp   |             | uLisp   |             |
|---------|-------------|---------|-------------|
| `:cs`   | CS   (GP15) | `:sck`  | SCK  (GP14) |
| `:mosi` | MOSI (GP12) | `:miso` | MISO (GP35) |
| `:sda`  | SDA  (GP18) | `:scl`  | SCL  (GP21) |
| `:rxd`  | RXD  (GP26) | `:txd`  | TXD  (GP13) |
|         | GND         |         | 3.3V        |

![](/docs/p3_header.jpg)

## RP2040 Pinout
(as seen from behind)
| uLisp   |      | uLisp   |             |
|---------|------|---------|-------------|
|         | VBUS |         | GP0 (ESP32) |
|         | VSYS |         | GP1 (ESP32) |
|         | GND  |         | GND         |
|         | 3.3V | `:gp2`  | GP2         |
|         | 3.3V | `:gp3`  | GP3         |
|         | VREF | `:gp4`  | GP4         |
| `:gp28` | GP28 | `:gp5`  | GP5         |
|         | GND  |         | GND         |
| `:gp27` | GP27 | `:gp6`  | GP6         |
| `:gp26` | GP26 | `:gp7`  | GP7         |
|         | RST  | `:gp8`  | GP8         |
| `:gp22` | GP22 | `:gp9`  | GP9         |
|         | GND  |         | GND         |
| `:gp21` | GP21 | `:gp10` | GP10        |
| `:gp20` | GP20 | `:gp11` | GP11        |
| `:gp19` | GP19 | `:gp12` | GP12        |
| `:gp18` | GP18 | `:gp13` | GP13        |
|         | GND  |         | GND         |
| `:gp17` | GP17 | `:gp14` | GP14        |
| `:gp16` | GP16 | `:gp15` | GP15        |

![](/docs/p1_p2_p5_headers.png)

## Motion Sensor (MPU-6500)



## Microphone (SPK0838HT4H)
