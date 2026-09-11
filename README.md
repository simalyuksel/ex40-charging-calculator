# Volvo EX40 Charging Calculator

A lightweight browser-based calculator for estimating charging time and energy consumption for a Volvo EX40.

## Demo

Live example page:

- https://www.simalyuksel.com/ex40

## Features

- Supports single-phase home outlets and three-phase wallboxes
- Calculates charging power from voltage and current values
- Accounts for an average 4.3% charging loss
- Applies the Volvo EX40's 11 kW AC charging limit
- Estimates charging time in three stages:
  - 0-80% at the full calculated power
  - 80-90% with reduced charging power
  - 90-100% with balancing and trickle charging time
- Shows estimated energy drawn from the grid and the expected finish time
- Works well on desktop and mobile browsers
- Uses a clean, single-page interface

## Usage

1. Open `index.html` in a modern browser.
2. Enter the current battery level.
3. Enter the target battery level.
4. Select the electrical connection type.
5. Enter the amperage selected in the vehicle.
6. Click **Calculate**.

The app displays results such as gross power, net charging rate, grid energy consumption, estimated duration, and finish time.

## Calculation Assumptions

The app is based on the following assumptions:

- Battery capacity: 79 kWh
- Charging efficiency: 95.7%
- Realistic under-load phase voltage: 225 V
- Single-phase charging uses effective values similar to 230 V
- Three-phase charging uses 3 x V x I
- Maximum AC charging power: 11 kW
- Reduced charging power above 80%
- Additional cell balancing time after 90%

These values are estimates. Actual charging times may vary depending on temperature, battery condition, electrical installation, vehicle software, and other environmental factors.

## Technical Overview

This project is a standalone HTML application with no build step or external dependencies.

## Project Structure

```text
.
├── index.html  # UI, styles, and JavaScript logic
├── ex40.png    # Volvo EX40 artwork used in the interface
├── README.md   # Project description
└── .gitignore  # Optional ignored files
```

## License

No license has been specified for this project yet.
