# Equity Protection EA

This is the code for the Equity Protection EA, developed by Forex Robot Easy Team. For detailed reviews and trading results of this product, visit the [Forex Robot Easy website](https://forexroboteasy.com/forex-robot-review/equity-protection-ea-review-the-position-manager-for-forex/).

## Global Variables

- `maxDrawdownLevel`: Maximum drawdown level, set to 0.1 (10%)
- `currentEquity`: Holds the current equity level

## Expert Advisor Start Function

The `OnInit()` function is called when the EA is initialized. It retrieves the current equity level using `AccountInfoDouble()` and prints the initial equity level.

## Expert Advisor Tick Function

The `OnTick()` function is called on every tick. It performs the following tasks:

1. `AdjustStopLoss()`: Calculates and adjusts the stop loss levels based on the equity level.
2. `MonitorEquityLevel()`: Monitors and tracks the equity level in real-time.
3. `CheckDrawdownLevel()`: Sets and manages the maximum drawdown level for closing positions.

## Calculate and Adjust Stop Loss Levels

The `AdjustStopLoss()` function calculates the stop loss levels based on the current equity level. It sets the stop loss level for all open positions using `PositionModify()`.

## Monitor and Track Equity Level

The `MonitorEquityLevel()` function retrieves the current equity level using `AccountInfoDouble()` and checks if it has changed significantly. If it has, an alert or notification is generated.

## Set and Manage Maximum Drawdown Level for Closing Positions

The `CheckDrawdownLevel()` function calculates the current drawdown level and checks if it exceeds the maximum drawdown level. If it does, all open positions are closed using `PositionClose()` and an alert or notification is generated.

## Expert Advisor Deinit

The `OnDeinit()` function is called when the EA is removed from the chart. It prints the final equity level.

Please note that Forex Robot Easy is not the official developer of this product. This code is provided as a sample that can work as described in the product. To find the official developer of this product, please use MQL5.
