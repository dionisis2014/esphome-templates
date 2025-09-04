# ESPHome Templates

Personal collection of ESPHome package templates to be used for quick and easy configuration of new devices.

## Board support

| Vendor       | Board  | Chip     | Built-in LED | BOOT Button | Notes          |
|--------------|--------|----------|:------------:|:-----------:|----------------|
| OEM          | DevKit | ESP32    |      ✓       |      ✓      |                |
| OEM          | DevKit | ESP32-S3 |      ✓       |      ✓      | Type-C version |
| Seeed Studio | Xiao   | ESP32-C6 |      ✓       |      ✓      |                |

## Module description

### base.yaml

The base configuration with common elements between all devices.

| Name                 | Type             | Default value  | Description                                   |
|----------------------|------------------|----------------|-----------------------------------------------|
| `node_name`          | string           | `esphome-node` | The ESPHome node name (used as id)            |
| `node_friendly_name` | string           | `ESPHome Node` | The ESPHome node friendly (used in dashboard) |
| `variant`            | string           | `esp32`        | The ESP32 chip variant                        |
| `gpio_led`           | string \| number | `GPIO2`        | The GPIO that the builtin LED is connected to |
| `gpio_usrbtn`        | string \| number | `GPIO0`        | The GPIO that the boot button is connected to |

### wifi.yaml

Enables Wi-Fi connectivity.

### thread.yaml

Enables the Thread connectivity.

> [!WARNING]
> MUST specify the network information or TLV in the `openthread` block.

### improv.yaml

Enables setting the Wi-Fi credentials via Bluetooth or serial.

### proxy.yaml

Enabled the Bluetooth proxy functionality for Home Assistant.
