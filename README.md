# Currency Forward Spread Curve

Similar to interest rate curves, FX curves can be categorized into market observed FX curves and derived FX curves. The market observable FX curves are also called FX forward points or FX forward spreads or FX forward curves, while the derived FX curves are also known as currency yield curves or currency implied forward curves.

FX forward points are defined as the relationship between FX forward spreads, in basis points, and delivery dates. Usually, an FX forward rate is quoted as FX forward spread, the number of basis points (called DP in FX convention), against the current FX spot rate for a future delivery date. Given FX forward points/spreads, FX forward rates can be very easily determined.

FX forward points/spreads or FX curves mainly use market observable quotes for each curve point directly except a few derivations, such as calculating the settlement dates for the given underlying tenors, and deriving ON (overnight) and TN (tomorrow next) points for FX market conventions.

FX forward spreads cannot be used to price FX trade directly. Thus, one needs to bootstrap FX forward spreads into currency yield curves that are used to value FX trades in the FX market. Currency yield curve (or currency zero rate curve or currency implied forward curve or currency derived curve) is defined as the relationship between currency yields-to-maturity and maturities.

In FX market, one key is to compute FX forward rate at any future date. The formula is called the interest rate parity given by

Please note that the currency interest rates in the FX market are different from the interest rates (for discounting or forecasting) in other markets. The interest rate curves in other markets (let us call them the IR yield curves) are bootstrapped from swap rate curves, while the currency interest rate curves in the FX makret (let us call them the FX yield curves) are derived from the USD yield curve and FX forward spreads.

In the USD/CAD currency pair, for instance, the FX yield curve in USD and the IR yield curve in USD are the same because the USD yield curve acts as the base reference curve. But the FX yield curve in CAD is different from the IR yield curve in CAD shown below:

FinPricing provides the market data of both FX forward points and FX yield curves for a broad range of currency pairs. It also offers FX curve construction tools for user to build their own FX curves.

Click the Data tab at the top-left corner of the application. Then, expend Data -> FxData -> FxCurve and click the Construct button.

A selection template window pops up. Fill the Base Currency in Column 1 (e.g., USD), Underlying Currency in Column 4 (e.g., CAD) and Curve Date in Column 5 (e.g., 2/8/2018). All of them are in the last rown. Then click the Go button.

You can find more details at
https://finpricing.com/faq/fxCurve.html

