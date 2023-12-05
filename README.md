# Neuro Scalper EA MT4

## Developer: Forex Robot Easy Team
## Developer's Site: [forexroboteasy.com](https://forexroboteasy.com)

---

This code is a sample implementation of the Neuro Scalper EA MT4, developed by the Forex Robot Easy Team. It is an Expert Advisor (EA) that can be used on the MetaTrader 4 platform for automated trading in the forex market.

### Required Libraries

The code includes the following required libraries:

- Trade - This library provides functions for executing trades.
- NeuroScalper - This library contains the Neuro Scalper indicator and its related functions.

### Global Variables

- `CTrade trade` - Trade object for executing trades.
- `CNeuroScalper neuroScalper` - Neuro Scalper indicator object.
- `bool isOptimizationMode` - Flag to indicate optimization mode.

### Initialization

The `OnInit()` function is called when the EA is initialized. In this function, the Neuro Scalper indicator is set up using the `neuroScalper.Init()` function. The `IsOptimization()` function is used to determine if the EA is in optimization mode. If it is, the optimization parameters are set using the `neuroScalper.SetOptimizationParameters()` function.

### Market Tick Handling

The `OnTick()` function is called on each tick of the market. In this function, the code checks for bullish and bearish divergence using the `neuroScalper.CheckDivergence()` function. Based on the divergence, buy and sell signals are generated using the `neuroScalper.IsBullishDivergence()` and `neuroScalper.IsBearishDivergence()` functions, and trades are executed using the `trade.Buy()` and `trade.Sell()` functions.

### Bar Handling

The `OnBar()` function is called at the end of each bar. In this function, the code automatically finds the best values for trading on the EUR/USD 1-hour timeframe if the EA is not in optimization mode and the symbol and period match the specified conditions. This is done using the `neuroScalper.AutoOptimize()` function.

### Deinitialization

The `OnDeinit()` function is called when the EA is deinitialized. In this function, resources are cleaned up using the `neuroScalper.Deinit()` function.

---

Please note that ForexRobotEasy is not the official developer of this product. We only provide a sample code that can work as described in this product. For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/review-neuro-scalper-ea-mt4-a-professional-forex-traders-perspective/). To find the official developer of this product, please refer to MQL5.
