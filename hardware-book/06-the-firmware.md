# Chapter 6 — The Firmware

[← Back to Table of Contents](./README.md) · [Previous: The Build](./05-the-build.md) · [Next: Calibration and Testing →](./07-calibration.md)

---

> The software that runs on the hardware. Flashing, configuration, and architecture.
> Write for someone who can program but hasn't worked with this specific platform.
>
> **Skip this chapter** if the project is purely mechanical with no programmable components.

## Platform

| Item | Value |
|------|-------|
| MCU | {e.g. ESP32-S3} |
| Framework | {e.g. Arduino, ESP-IDF, Zephyr, MicroPython} |
| Language | {e.g. C++, Rust, Python} |
| IDE | {e.g. PlatformIO, Arduino IDE} |

## First Flash

*Get firmware onto the hardware for the first time.*

### Prerequisites

```bash
# Install toolchain
{e.g. pip install platformio}
```

### Build and Flash

```bash
# Connect USB to MCU
# Build
{e.g. pio run}

# Flash
{e.g. pio run --target upload}

# Monitor serial output
{e.g. pio device monitor}
```

### Expected Output

```
*What they should see on first boot — serial output, LED behavior, etc.*
```

## Configuration

*How to configure the firmware for different setups.*

| Setting | Default | Description |
|---------|---------|-------------|
| {e.g. WIFI_SSID} | {none} | {WiFi network name} |
| {e.g. STEP_PIN} | {25} | {Stepper motor step pin} |
| {e.g. SENSOR_INTERVAL_MS} | {1000} | {Sensor read interval} |

## Firmware Architecture

```
├── src/
│   ├── main.{ext}         # Entry point, setup, main loop
│   ├── drivers/            # Hardware abstraction
│   │   ├── {motor}.{ext}  # {Motor control}
│   │   └── {sensor}.{ext} # {Sensor reading}
│   ├── app/                # Application logic
│   └── comms/              # Communication (WiFi, Serial, BLE)
├── include/                # Headers / config
├── lib/                    # Local libraries
└── platformio.ini          # Build configuration
```

## Key Modules

### {Module: e.g. Motor Control}

**What it does:** {One sentence}

**Key functions:**
- `{function_name}()` — {What it does}
- `{function_name}()` — {What it does}

**Hardware interaction:** {Which pins, protocols, timing constraints}

### {Module: e.g. Sensor Reading}

**What it does:** {One sentence}

**Key functions:**
- `{function_name}()` — {What it does}

**Hardware interaction:** {Pins, protocols, timing}

## Communication Protocol

*If the device communicates externally — serial commands, WiFi API, BLE services.*

### Commands / API

| Command | Description | Example |
|---------|-------------|---------|
| {e.g. `MOVE X Y`} | {Move to position} | {`MOVE 100 50`} |
| {e.g. `STATUS`} | {Report current state} | {`STATUS`} |

## OTA Updates

*If applicable — how to update firmware without physical access.*

```bash
# {OTA update command}
```

---

[Next: Calibration and Testing →](./07-calibration.md)
