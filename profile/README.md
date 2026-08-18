# Internet of Pins

Static, compositional, zero-cost abstractions for modern C++ on embedded systems.

## Philosophy

Every abstraction compiles away. No virtual dispatch, no heap allocation, no runtime overhead — just the logic your hardware needs, composed at compile time from small, reusable building blocks.

Built on [HAPI](https://github.com/InternetOfPins/HAPI) — a zero-overhead heterogeneous chain and query framework — each library adds one orthogonal concern and stacks cleanly with the rest.

## Libraries

| Library | Description |
|---------|-------------|
| [HAPI](https://github.com/InternetOfPins/HAPI) | Heterogeneous chain, query, and rule engine — the foundation |
| [OneOutput](https://github.com/InternetOfPins/OneOutput) | Output pipeline API — put, nl, setPos, cursor |
| [OneData](https://github.com/InternetOfPins/OneData) | Typed data wrappers — Data, Watch, NumRange, StaticText |
| [OneItem](https://github.com/InternetOfPins/OneItem) | Menu item definitions — fields, actions, labels |
| [OneMenu](https://github.com/InternetOfPins/OneMenu) | Composable menu system — navigation, rendering, input |
| [OneParse](https://github.com/InternetOfPins/OneParse) | Zero-overhead parser combinators |
| [OneBit](https://github.com/InternetOfPins/OneBit) | Bit-level pin and port abstractions |
| [OnePin](https://github.com/InternetOfPins/OnePin) | Digital pin API — InPin, OutPin, IOPin |
| [OneChip](https://github.com/InternetOfPins/OneChip) | MCU peripheral abstractions — ISR, port allocation |
| [OneBus](https://github.com/InternetOfPins/OneBus) | Communication bus abstractions — SPI, I2C/TWI, UART, 1-Wire |
| [OneInput](https://github.com/InternetOfPins/OneInput) | Input event chains — debounce, click/hold, encoder, analog joystick |
| [OneSensor](https://github.com/InternetOfPins/OneSensor) | Sensor drivers parameterized on bus and chip — DS18B20, MPU6050 |
| [OneIO](https://github.com/InternetOfPins/OneIO) | Physical device drivers — displays, sensors, EEPROM, PWM, RTC, RF |
| [OneHLS](https://github.com/InternetOfPins/OneHLS) | HLS-synthesizable DSP and control components |

## Targets

AVR (Uno, Mega, ATtiny13/45/85) · STM32 · nRF52 · ESP32 · ESP8266 · CH32V003 (compile-verified) · Linux/native

Built and tested via PlatformIO.

## Hardware synthesis (HLS)

The "compiles away" claim has been checked against more than a traditional compiler: HAPI, OneParse, OneBit, OneData, OneItem, and OneOutput have been run through High-Level Synthesis (Bambu/PandA, with Vitis HLS scaffolding in progress) — turning the same template-composed C++ into real RTL. The heterogeneous chain, query, and rule machinery survives synthesis intact, confirming the zero-overhead design holds down to hardware, not just object code. [OneHLS](https://github.com/InternetOfPins/OneHLS) builds on this with type-agnostic DSP and control components meant to be synthesized directly.

## Requirements

C++17 or later. No STL dependency on AVR targets.
