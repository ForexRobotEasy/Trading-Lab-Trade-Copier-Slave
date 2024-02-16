# Trading Lab Trade Copier Slave

This code is a Trade Copier Slave that allows you to copy trades from a master terminal to multiple slave terminals. It is developed by Forex Robot Easy Team and can be used to streamline forex trading with Metatrader 5.

## How it Works

1. The code establishes a connection to the master terminal using the `trade.Connect()` function. Make sure to replace `'MasterTerminalIP'` with the IP address of your master terminal and `12345` with the desired port number.

2. It subscribes to trade signals from the master terminal using the `trade.SubscribeToTradeSignals()` function.

3. In the `OnTick()` function, the code checks for new trade signals from the master terminal using the `trade.CheckForTradeSignals()` function.

4. If new trade signals are available, the code retrieves the trade signals using the `trade.GetNextTradeSignal()` function and then calls the `CopyTradeSignalToSlaves()` function to copy the trade signal to the slave terminals.

5. The `CopyTradeSignalToSlaves()` function executes the trade on each slave terminal. It calculates the lot size for each slave terminal using the `CalculateLotSize()` function and then calls the `trade.ExecuteTrade()` function to execute the trade.

6. The `MonitorStopLossAndTakeProfit()` function is used to monitor and update the stop loss and take profit levels on the slave terminals. It retrieves the open positions on the slave terminals using the `trade.GetPositions()` function and then calls the `trade.UpdatePositionSLTP()` function to update the stop loss and take profit levels.

7. The code also includes an error handling function `OnTradeError()` to handle trade execution errors.

8. The main loop in the `OnStart()` function continuously calls the `OnTick()` function and sleeps for 1 second between iterations. You can adjust the sleep time based on your requirements.

## Product Description

This Trade Copier Slave is designed to work with the Trading Lab Trade Copier system. It allows you to copy trades from a master terminal to multiple slave terminals, streamlining your forex trading process. The code is developed by Forex Robot Easy Team and can be used with Metatrader 5.

To use this Trade Copier Slave, you need to set up a connection with the master terminal and subscribe to trade signals. Once connected, the code will continuously check for new trade signals from the master terminal and copy them to the slave terminals. It also monitors and updates the stop loss and take profit levels on the slave terminals.

Please note that ForexRobotEasy is not the official developer of this product. We are only providing sample code that can work as described in the product. To find the official developer of this product, please use MQL5.

For detailed reviews and trading results of this product, you can visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/trading-lab-trade-copier-review-streamline-forex-with-metatrader5/).
