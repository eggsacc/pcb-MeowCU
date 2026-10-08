<div align="center">

# MeowCU

![MCU](https://img.shields.io/badge/MCU-STM32F405RGT6-03234B?style=flat-square&logo=stmicroelectronics&logoColor=white)
![PCB](https://img.shields.io/badge/PCB-4--layer-2E8B57?style=flat-square)
![EDA](https://img.shields.io/badge/KiCad-314CB0?style=flat-square&logo=kicad&logoColor=white)


4-layer **STM32F405RGT6 MeowCU** 🐱 (MCU) dev module with commonly used peripherals broken out for easy access, and a dedicated CAN transceiver. Also includes 2 user programmable buttons and mini OLED display.

>3D render - Front

<img src="assets/v1.7-render.png" width="720" alt="STM32F4 dev module render">

>Back

<img src="assets/v1.7-render-back.png" width="720" alt="STM32F4 dev module render">


## Layout (all layers)
<img src="assets/v1.7-layout.png" width="720" alt="STM32CubeMX pin map">
</div>


## MCU Pinout

<div align="center">
<img src="assets/stm32_ioc.png" width="720" alt="STM32CubeMX pin map">

| Breakout / feature | Peripheral | Pin mapping |
|---|---|---|
| **UART header** | `USART3` | TX &rarr; `PC10`<br>RX &rarr; `PC11` |
| **SPI header** | `SPI1` | CS &rarr; `PA4`<br>SCK &rarr; `PA5`<br>MISO &rarr; `PA6`<br>MOSI &rarr; `PA7` |
| **I2C header** | `I2C1` | SCL &rarr; `PB6`<br>SDA &rarr; `PB7` |
| **CAN screw terminal** | `CAN1` (SN65HVD230) | TX &rarr; `PB9`<br>RX &rarr; `PB8` |
| **USB-C** | `USB_OTG_FS` | D&minus; &rarr; `PA11`<br>D+ &rarr; `PA12` |
| **SWD header** | `SYS` | SWDIO &rarr; `PA13`<br>SWCLK &rarr; `PA14` |
| **3-phase PWM header** | `TIM1` | <table><tbody><tr><td align="right">CH1 &rarr;</td><td><code>PA8</code></td><td align="right">&emsp;C1N &rarr;</td><td><code>PB13</code></td></tr><tr><td align="right">CH2 &rarr;</td><td><code>PA9</code></td><td align="right">&emsp;C2N &rarr;</td><td><code>PB0</code></td></tr><tr><td align="right">CH3 &rarr;</td><td><code>PA10</code></td><td align="right">&emsp;C3N &rarr;</td><td><code>PB1</code></td></tr></tbody></table> |
| **OLED** (on-board) | `I2C2` | SCL &rarr; `PB10`<br>SDA &rarr; `PB11` |
| **Utility buttons** (on-board) | `GPIO` / `EXTI` | L button &rarr; `PA2`<br>R button &rarr; `PA3` |
| **Crystal** (25MHz) | `RCC` HSE | OSC_IN &rarr; `PH0`<br>OSC_OUT &rarr; `PH1` |
| **GPIO header** (2&times;10) | free GPIO | <table><tbody><tr><td align="right">1 &rarr;</td><td><code>3.3V</code></td><td align="right">&emsp;2 &rarr;</td><td><code>3.3V</code></td></tr><tr><td align="right">3 &rarr;</td><td><code>5V</code></td><td align="right">&emsp;4 &rarr;</td><td><code>5V</code></td></tr><tr><td align="right">5 &rarr;</td><td><code>GND</code></td><td align="right">&emsp;6 &rarr;</td><td><code>GND</code></td></tr><tr><td align="right">7 &rarr;</td><td><code>PB4</code></td><td align="right">&emsp;8 &rarr;</td><td><code>PB3</code></td></tr><tr><td align="right">9 &rarr;</td><td><code>PC12</code></td><td align="right">&emsp;10 &rarr;</td><td><code>PC2</code></td></tr><tr><td align="right">11 &rarr;</td><td><code>PC3</code></td><td align="right">&emsp;12 &rarr;</td><td><code>PA0</code></td></tr><tr><td align="right">13 &rarr;</td><td><code>PA1</code></td><td align="right">&emsp;14 &rarr;</td><td><code>PC9</code></td></tr><tr><td align="right">15 &rarr;</td><td><code>PC8</code></td><td align="right">&emsp;16 &rarr;</td><td><code>PC7</code></td></tr><tr><td align="right">17 &rarr;</td><td><code>PC6</code></td><td align="right">&emsp;18 &rarr;</td><td><code>PB15</code></td></tr><tr><td align="right">19 &rarr;</td><td><code>PB14</code></td><td align="right">&emsp;20 &rarr;</td><td><code>PB12</code></td></tr></tbody></table> |

**Buttons are active-low to GND (3V3 pull-up).*
</div>


## Power mux

The external 5V pin and USB `vbus` are separate rails; a power mux IC (TPS2116) automatically switches to the external 5V rail when connected.

---

<div align="center">
Designed by <b>@eggsacc</b> · MeowCU V1.6<br>
Updated 09/10/2026
</div>
