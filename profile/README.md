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
| [OneBus](https://github.com/InternetOfPins/OneBus) | Communication bus abstractions |
| [OneSensor](https://github.com/InternetOfPins/OneSensor) | Sensor drivers parameterized on bus and chip — DS18B20, MPU6050 |
| [OneIO](https://github.com/InternetOfPins/OneIO) | Physical device drivers — displays, sensors, actuators |

## Targets

AVR (Uno, Mega, ATtiny13/45/85) · STM32 · nRF52 · ESP32 · ESP8266 · CH32V003 (compile-verified) · Linux/native

Built and tested via PlatformIO.

## Requirements

C++17 or later. No STL dependency on AVR targets.
