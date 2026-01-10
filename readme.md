# Gold Label Indicator  
### by @imriazul

A **time-based Gold (XAUUSD) TradingView indicator** that calculates a projected daily price range from a specific opening candle and visualizes it using a box and key internal levels.

---

## 📌 Overview

**Gold Label** is designed to capture a precise **daily opening moment** on Gold and project a mathematically calculated price range forward on the chart.

The range is derived using a **square-root expansion method** and is visualized with:

- A projected price **range box**
- A **midpoint** level
- Two internal equilibrium levels (**37.5% & 62.5%**)

This tool is best suited for **intraday structure, range trading, and reaction-based analysis**.

---

## 🪙 Supported Markets

The indicator activates **only on Gold symbols**:

- `XAUUSD`
- `GOLD`
- Any symbol containing `XAU`

All other instruments are ignored automatically.

---

## ⏱ Supported Timeframes

The indicator works on the following chart timeframes:

- **5 Minutes**
- **15 Minutes**
- **30 Minutes**

> ⚠️ The calculation always uses the **opening price of the trigger candle** on the active timeframe.

---

## 🌍 Time Logic (Asia/Dhaka)

The system runs **once per day** at a fixed Dhaka time.

### DST Toggle

A setting is provided to handle Daylight Saving Time behavior.

| DST Setting | Trigger Time (Dhaka) |
|------------|---------------------|
| **ON** (default) | `06:00 AM` |
| **OFF** | `07:00 AM` |

Only the candle that **opens exactly at the configured time** is used.

---

## 🧮 Core Calculation Logic

At the trigger candle:

1. The **opening price** is captured  
2. Square-root is applied  
3. A fixed offset of `±0.105` is added  
4. Values are squared back into price  

This produces:

- **Upper Range**
- **Lower Range**

From the range, the following levels are calculated:

- **Midpoint (50%)**
- **Lower Equilibrium (37.5%)**
- **Upper Equilibrium (62.5%)**

---

## 📦 Visual Elements

### 1️⃣ Range Box
- **Top:** Upper range  
- **Bottom:** Lower range  
- **Width:** 24 bars forward from the trigger candle  

### 2️⃣ Horizontal Levels
- Midpoint (50%)
- 37.5% level
- 62.5% level

All lines extend **exactly the same duration** as the box.

---

## 📈 Moving Averages

The indicator also plots:

- **EMA 9**
- **EMA 15**

These EMAs are **always visible** and independent of the time-based logic.

---

## ✅ Execution Rules (Strict)

The indicator logic executes **only when all conditions are met**:

- Symbol is Gold (XAU)
- Time matches the configured Dhaka trigger time
- Chart timeframe is **5m, 15m, or 30m**

If **any condition fails**, no drawing occurs.

---

## 🎯 Intended Use

This indicator is intended for:

- Daily range framing
- Intraday Gold trading
- Reaction-based entries
- EMA structure confirmation
- Session-based market analysis

> 🚫 This is **not** a buy/sell signal generator.

---

## ⚠️ Notes & Limitations

- Each trigger creates a new projected range
- Drawing objects are not stored in arrays
- Excessive historical drawings may reach TradingView object limits

---

## 👤 Author

**@imriazul**  
Custom TradingView indicator for **Gold (XAUUSD)**