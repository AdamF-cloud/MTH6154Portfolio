# 1. Interest rates

[Back to contents](../README.md)

## Summary
Context: 

Central Banks (Federal Reserve, ECB, BoE) set official base rates for borrowing. The base rate is primarily an overnight deposit rate. Select financial institutions are able to deposit overnight at this rate receiving set interest on funds in the bank overnight. 

We use the SONIA, the Sterling Overnight Index Average for ? Before this we used to use LIBOR. 

Other institutions are able to borrow, and lend through these banks, creating a spread, measured in BP Basis Points.

Basis points are defined as 1 bp = 0.01% = 0.0001

1: 
We have an annual nominal rate, r. The amount of times an interest compounds, n. And our initial payment P

 We will gain After 1 year: 

 LATEX: P(!+r/n)^n

 After now T, years we will gain: 

 LATEX: Show working out from each year combining into T years.

Example 1
As of 04/11/26, the Base Rate set by the BoE is 3.75.
Bank A, paying £10 million for a 1 day deposit will earn tomorrow:

LATEX: 10m(1+3.75/365)^365/365 = ?

At 3.75% = r, in 2 years time he will earn, with interest compounding every 6 months:

LATEX: 10m(1+3.75/2)^2*2 = ?

If client drops 10m at bank A, which bank A lends out at 3.72%, A earns a risk free spread of 

LATEX: Spread = 3.75% - 3.72% = 0.03% = 3 BP

If we are to let N compound every minute, what about every second, millisecond, what happens? Increasing n to infinity gives us the limit. 

LATEX sum to infinity = e, then show how that compounds Pe^rT

We should be questioning the point of nominal rates with different frequencies, and standardise them to the net percentage increase over 1 year, we show this through effective annual rate given by:

LATEX reff = (1+r/n)^n -1

For a continuously compounding rate: 

LATEX reff = e^r -1 

2: Variable rates & Yield Curve

Rates may continuously vary over time, and will follow a differential equation

LATEX P'(t)/P(t) = R(t) implies through integration, P(t) = P(0) *e^int(0totr(s)ds

we can take this average of LATEX r(t) as rbar(t) = 1/t int0to t r(s)ds, with P(t) = e^rbar(t)*t
and also apply this to an effective rate horizon 

LATEX reff(T) = e^rbar(T) - 1

Example to use everything we have done.

An investor desposits £2000 (P(0) = 2000) for t = 3 years, into a bond paying: r(t) = 0.03 + 0.02t
We want to find our average yield curve, and how much we will earn at p3

LATEX rbar(3) = 1/3int $$\overline{r}(3) = \frac{1}{3} \int_0^3 (0.03 + 0.02u) \, du = \frac{1}{3} \left[ 0.03u + 0.01u^2 \right]_0^3$$   $$\overline{r}(3) = \frac{1}{3} \big( 0.03(3) + 0.01(9) \big) = \frac{1}{3} (0.09 + 0.09) = \frac{0.18}{3} = 0.06 \quad (6.0\%)$$

$$P(3) = P(0)e^{\overline{r}(3) \times 3} = 2{,}000 e^{0.06 \times 3} = 2{,}000 e^{0.18}$$ = ???

We could also find our effective annual rate: 

bettermake$$r_{\text{eff}} = e^{\overline{r}(3)} - 1 = e^{0.06} - 1 \approx 1.061837 - 1 = \mathbf{6.18\%}$$

We can analyse inflation, through CPI or RPI to see how much the value of our money decreases over time. Whilst our investment may grow at 

LATEX 1 + reff, we also lose value through inflation at 1 + rinf. Dividing that gives us our effective growth formula 1 + r_real, which we can minus -1 to show r_real = XXXdoXXX
Please see spreadsheet for an example on this please, and more information.













Maths is written between dollar signs. For example `$A = P(1+i)^n$` shows
as $A = P(1+i)^n$, and a displayed formula uses double dollars:

$$
\left(1+\frac{i^{(m)}}{m}\right)^m = 1+i
$$

## My example

A situation you made up (your own numbers, not the ones in the lecture
notes), worked step by step.

## Solved exercises

### Exercise 1.x (from Exercise Sheet 1)

Question, then your solution.

## Spreadsheet

[01-InterestRates.xlsx](../spreadsheets/01-InterestRates.xlsx): what it
does, which cells to change and what to look at.
