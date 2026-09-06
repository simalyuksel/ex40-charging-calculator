# Volvo EX40 Charging Calculator

A lightweight, browser-based calculator for estimating the charging time and energy consumption of a Volvo EX40.

## Features

- Supports single-phase home outlets and three-phase wallboxes
- Calculates charging power from voltage and amperage
- Accounts for an estimated 4.3% charging loss
- Applies the Volvo EX40's 11 kW AC charging limit
- Estimates charging time in three stages:
  - 0-80% at full calculated power
  - 80-90% with reduced charging power
  - 90-100% with balancing and trickle charging time
- Shows estimated energy drawn from the grid and the expected finish time
- Responsive layout for desktop and mobile browsers

## Usage

1. Open `index.html` in a modern web browser.
2. Enter the current battery level.
3. Enter the target battery level.
4. Select the electrical connection type.
5. Enter the amperage selected in the vehicle.
6. Click **Calculate**.

The calculator displays the estimated net charging power, energy drawn from the grid, charging duration, and estimated finish time.

## Technical Details

This project is a standalone HTML application with no build step or external dependencies.

The main assumptions are:

- Battery capacity: 79 kWh
- Charging efficiency: 95.7%
- Single-phase voltage: 230 V
- Three-phase voltage: 400 V
- Maximum AC charging power: 11 kW
- Reduced power after 80% state of charge
- Additional balancing time after 90% state of charge

These values are estimates. Actual charging times may vary depending on temperature, battery condition, electrical installation, vehicle software, and other charging conditions.

## Project Structure

```text
.
├── index.html  # Application markup, styles, and JavaScript
└── ex40.png    # Volvo EX40 image used by the interface
```

## License

No license has been specified for this project yet.
