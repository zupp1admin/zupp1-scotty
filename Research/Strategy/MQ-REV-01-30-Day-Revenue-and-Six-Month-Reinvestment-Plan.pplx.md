# MQ-REV-01 — 30-Day Revenue and Six-Month Reinvestment Plan

**Status:** Proposed for bridge approval  
**Prepared for:** USS Zupp1  
**Objective:** Generate the first attributable revenue within 30 days using a maximum initial Meta advertising budget of R$20 per day, then use verified marketing profit to finance a controlled six-month reinvestment loop.  
**Operating constraint:** Current contribution margin is approximately 10%.

## Executive summary

**FACT:** The initial media ceiling is R$600 over 30 days. At a 10% contribution margin, each R$100 of product revenue contributes only R$10 before advertising. Therefore, advertising breaks even at a 10.0× revenue-to-ad-spend ratio if the 10% margin already includes every variable cost except advertising.

**ASSESSMENT:** Achieving one or more sales within 30 days is plausible, but achieving repeatable paid-media profitability is a much harder objective. The campaign must not interpret revenue, clicks, or an isolated sale as proof of a viable acquisition system.

**RECOMMENDATION:** Use the first month to identify one credible product-audience-message path. Concentrate the budget on one hero product or tightly related product family, one landing path, one audience hypothesis, and no more than two sequential creative treatments.

**RECOMMENDATION:** Do not release money into the six-month loop until profit is verified after discounts, cancellations, refunds, payment fees, taxes, shipping subsidies, and other variable costs. Revenue is not reinvestable profit.

## Strategic objective and decision

The 30-day mission answers one question:

> Can Zupp1 acquire a customer through Meta while recovering the advertising cost from the order's actual contribution margin?

The campaign has three success levels:

| Level | Definition | Meaning |
|---|---|---|
| Revenue signal | At least one correctly attributed, fulfilled sale | The website can convert some paid traffic |
| Repeatability signal | At least two sales from the same product-audience-message path without operational failure | The result may be reproducible, but is not yet statistically established |
| Economic signal | Settled contribution from attributed orders exceeds advertising spend | The path may qualify for controlled reinvestment |

**ASSESSMENT:** With R$600, Zupp1 is unlikely to obtain enough purchases for formal statistical proof. The proper output is a decision-grade directional signal and a clean record of what happened.

## Economics governing the mission

Let:

- \(A\) = advertising spend
- \(R\) = attributed settled revenue
- \(m\) = contribution margin after non-advertising variable costs
- \(X\) = refunds, chargebacks, discounts, shipping subsidies, or other variable costs not already included in the margin
- \(P\) = marketing profit

\[
P = (R \times m) - A - X
\]

At \(m = 10\%\) and \(X = 0\):

\[
\text{Break-even ROAS} = \frac{1}{0.10} = 10.0
\]

\[
\text{Maximum allowable CAC} = \text{AOV} \times 0.10
\]

### Break-even order requirements for the first month

| Average order value | Maximum allowable CAC | Orders needed to recover R$600 |
|---:|---:|---:|
| R$100 | R$10 | 60 |
| R$150 | R$15 | 40 |
| R$200 | R$20 | 30 |
| R$250 | R$25 | 24 |
| R$300 | R$30 | 20 |
| R$500 | R$50 | 12 |
| R$750 | R$75 | 8 |
| R$1,000 | R$100 | 6 |

**ASSESSMENT:** Low-ticket products with a 10% contribution margin are poor candidates for cold paid acquisition because their allowable customer acquisition cost is extremely small.

**RECOMMENDATION:** Select the first hero product using this order:

1. Highest verified contribution reais per order, not highest revenue.
2. Strong purchase intent and a clearly explainable customer problem.
3. Reliable stock, delivery, returns, and support.
4. A landing page that can educate without delaying the purchase decision.
5. A price and shipping proposition that remain competitive after all disclosed costs.

**INTELLIGENCE GAP:** The current average order value, product-level margin, shipping subsidy, refund rate, payment fee, taxes, and repeat-purchase economics have not been verified. No product should enter the campaign until these values are recorded.

## Preflight gate

The 30-day paid period begins only after this gate passes.

### Required actions

- Select one hero product or one tightly related product family.
- Calculate actual contribution reais per order.
- Confirm product availability, delivery promise, returns process, and customer-support readiness.
- Complete a real test order on mobile and desktop.
- Verify events for landing-page view, product view, add to cart, checkout initiation, purchase, value, currency, and product identifier.
- Verify that WooCommerce order revenue and Meta purchase values reconcile.
- Apply UTM parameters and confirm analytics receives them.
- Create a one-page daily ledger for spend, sessions, funnel events, orders, revenue, contribution, refunds, and anomalies.

Meta documents that its Pixel can track visitor actions and standard conversion events, including product search, product view, and purchase; tracked conversions can be used to analyze the funnel and advertising return ([Meta Pixel conversion tracking](https://developers.facebook.com/docs/meta-pixel/implementation/conversion-tracking/)).

### Preflight stopping rule

**STOP:** Do not spend if a test purchase is missing, duplicated, assigned the wrong value or currency, or cannot be reconciled to the WooCommerce order.

## Weekly action plan

### Week 1 — Establish a clean baseline

**Budget ceiling:** R$140

**Actions**

- Launch one Sales campaign, one ad set, one audience hypothesis, one hero product, one landing path, and one primary creative.
- Optimize toward Purchase if tracking is reliable. Meta states that website purchase ads use Pixel activity to seek likely purchasers and may initially use upstream activity when purchase data is insufficient ([Meta website purchase ads](https://www.facebook.com/business/help/1104266309729652)).
- Keep message, offer, destination, and audience stable for the seven-day observation period unless a hard stopping rule is triggered.
- Review instrumentation and operational failures daily; review performance decisions after meaningful accumulated spend, not after individual hours.
- Record customer questions, support contacts, delivery concerns, and objections verbatim.

**Decision at week end:** Is the traffic qualified, is the landing path functioning, and is there any downstream intent?

### Week 2 — Isolate the largest bottleneck

**Budget ceiling:** R$140, released only if Week 1 has no hard-stop condition.

**Actions**

- Keep the winning or least-bad path unchanged.
- Change only the variable associated with the clearest bottleneck:
  - low qualified visits: creative hook or audience promise;
  - visits without product engagement: landing-page/message match;
  - product engagement without cart activity: offer, price, product clarity, or trust;
  - cart activity without checkout: shipping, urgency, or checkout friction;
  - checkout without purchase: payment, final cost, trust, or technical failure.
- If creative is the diagnosed bottleneck, replace the first creative with one new treatment. Do not create multiple audience and creative splits.

**Decision at week end:** Did the single intervention improve the next meaningful funnel step without degrading traffic quality?

### Week 3 — Attempt replication

**Budget ceiling:** R$140, released only if at least one credible downstream signal exists.

**Actions**

- Repeat the strongest product-audience-message path.
- Preserve the same offer and landing path long enough to test whether the signal reappears.
- Contact consenting buyers for a short post-purchase question: “What gave you enough confidence to buy?”
- Classify each sale as attributable, assisted, uncertain, or non-campaign.
- Calculate provisional marketing profit using settled order contribution, not platform-reported revenue alone.

**Decision at week end:** Is there a second independent purchase or a consistent sequence of high-intent actions supporting replication?

### Week 4 — Confirm economics or stop

**Budget ceiling:** R$140 for days 22–28, plus no more than R$40 for days 29–30.

**Actions**

- Direct remaining spend only to the best-supported path.
- Do not introduce a new product, audience, landing page, and creative simultaneously.
- Reconcile Meta, analytics, WooCommerce, payment, refund, and fulfillment records.
- Separate gross revenue, settled revenue, contribution, advertising spend, and marketing profit.
- Write the 30-day decision: scale cautiously, continue learning at the same cap, redesign the offer, or stop paid acquisition.

**Decision at day 30:** Has Zupp1 produced revenue, repeatability evidence, and positive settled marketing profit?

Meta notes that major changes to targeting, creative, optimization event, bid strategy, or prolonged pauses can return an ad set to learning; budget changes can also do so depending on their magnitude ([Meta learning-phase guidance](https://www.facebook.com/business/help/316478108955072)). This supports deliberate, infrequent changes rather than daily reaction.

## Measurement framework

### Primary metrics

| Metric | Formula | Decision supported |
|---|---|---|
| Settled attributed revenue | Paid and fulfilled revenue less cancellations and refunds | Whether the campaign created real revenue |
| Contribution reais | Settled revenue × verified product contribution margin | How much money exists before advertising |
| Marketing profit | Contribution reais − ad spend − excluded variable costs | Whether reinvestment is permitted |
| Blended ROAS | Settled attributed revenue ÷ ad spend | Whether the 10× break-even threshold is approached |
| CPA | Ad spend ÷ attributed customers | Whether acquisition fits product economics |
| Maximum allowable CAC | AOV × verified contribution margin | The hard economic ceiling |

### Diagnostic metrics

- Landing-page views and cost per landing-page view.
- Product-view rate from landing-page views.
- Add-to-cart rate from product views.
- Checkout-initiation rate from add-to-cart.
- Purchase rate from checkout initiation.
- Site purchase conversion rate.
- Average order value.
- Mobile page performance and checkout errors.
- Shipping-cost exposure and delivery estimate.
- Refunds, cancellations, chargebacks, and support contacts.
- New versus returning purchasers.
- Educational-content engagement before product engagement.

**ASSESSMENT:** CTR, impressions, reach, and low CPC may diagnose delivery or message resonance, but none establishes commercial success. They must never override contribution, CPA, and settled marketing profit.

### Evidence labels

- **FACT:** Directly observed in platform, analytics, order, payment, or support records.
- **ASSESSMENT:** Interpretation of observed evidence.
- **RECOMMENDATION:** Proposed action based on facts and assessments.
- **INTELLIGENCE GAP:** A value or causal explanation that cannot yet be verified.

## Stopping rules

### Immediate hard stops

Pause spending immediately if:

- purchase tracking is missing, duplicated, or materially inconsistent with WooCommerce;
- checkout or payment is failing;
- the advertised product is unavailable or its fulfillment promise is unreliable;
- displayed price, shipping, promotion, return policy, or disclosure is inaccurate;
- spend exceeds the approved daily or monthly ceiling;
- customer harm, misleading messaging, or policy risk is detected.

### Economic stops

- **Campaign stop:** Stop paid acquisition if cumulative spend reaches R$600 without a fulfilled attributed sale.
- **Path stop:** Stop a product-audience-message path without a sale when spend reaches the lower of the weekly budget ceiling or the greater of R$40 and two times the verified maximum allowable CAC. Strong checkout evidence may justify one additional controlled interval, documented before spending it.
- **Profit stop:** Do not reinvest when marketing profit is zero or negative.
- **Margin stop:** Stop and recalculate if actual contribution margin is below 10%.
- **Cash stop:** Do not use unsettled revenue, expected refunds, or supplier obligations as available advertising cash.

### Diagnostic stops

These are operating heuristics, not statistical proof:

- After 50 qualified landing-page views with zero add-to-cart events, pause and revise the product, offer, message, or landing match.
- After 10 add-to-cart events with zero checkout initiations, inspect cart, shipping, and checkout friction before more traffic.
- After 5 checkout initiations with zero purchases, inspect payment, final price, delivery, and trust before more traffic.
- If the sample is below these levels, label the result **INTELLIGENCE GAP — insufficient observations** rather than declaring a winner or loser.

### Scaling rules

- Do not scale from one isolated sale.
- Require positive settled marketing profit and at least two attributed fulfilled orders from the same path before any increase.
- Increase available advertising cash only through verified profit under the reinvestment formula.
- Avoid abrupt campaign edits; preserve a written before-and-after record for every change.
- Return to the prior budget or stop if trailing settled economics fall below break-even.

## Six-month reinvestment loop

### Calculation

For month \(t\):

\[
P_t = (R_t \times m_t) - A_t - X_t
\]

If the original advertising principal is recovered, marketing profit is nonnegative, and 100% of verified marketing profit is reinvested:

\[
A_{t+1} = A_t + P_t
\]

Equivalently:

\[
A_{t+1} = (R_t \times m_t) - X_t
\]

If \(P_t < 0\), automatic reinvestment stops. Release the next month's budget only after orders are settled and expected refunds, chargebacks, taxes, fees, fulfillment, and shipping obligations are reserved.

### Illustrative six-month paths

The following is arithmetic, not a forecast. It assumes a constant 10% contribution margin, no additional excluded costs, no delays, and total reinvestment of recovered advertising principal plus verified profit.

| Month | 8× ROAS status | 10× ROAS available spend | 12× ROAS available spend |
|---:|---:|---:|---:|
| 1 | R$600 invested; R$120 loss | R$600 | R$600 |
| 2 | STOP — no automatic reinvestment | R$600 | R$720 |
| 3 | STOP | R$600 | R$864 |
| 4 | STOP | R$600 | R$1,037 |
| 5 | STOP | R$600 | R$1,244 |
| 6 | STOP | R$600 | R$1,493 |
| Available after Month 6 | Not applicable | R$600 | R$1,792 |

**ASSESSMENT:** At 8× ROAS the first month loses R$120 and the automatic loop stops. At 10× it merely preserves the original advertising principal. At 12× it compounds, but slowly. Any excluded variable cost raises the true break-even ROAS above 10×.

### Weekly release control

Maintain four balances:

1. **Advertising principal:** the approved seed capital not yet spent.
2. **Revenue received:** cash collected, not automatically available.
3. **Reserve:** product costs, taxes, fees, delivery, refunds, and chargebacks.
4. **Reinvestment wallet:** only recovered advertising principal plus verified marketing profit.

At each weekly review:

- reconcile orders and excluded costs;
- keep unsettled orders in provisional status;
- release no more than the verified reinvestment wallet;
- retain the R$20 daily cap during the first month even if early profit appears;
- after day 30, set the next cap from settled economics rather than optimism.

## Bridge dashboard

The weekly bridge report should contain only:

1. Spend.
2. Settled attributed revenue.
3. Fulfilled attributed orders.
4. AOV.
5. Verified contribution margin and contribution reais.
6. CPA versus maximum allowable CAC.
7. Marketing profit.
8. Reinvestment wallet.
9. Largest funnel bottleneck.
10. Decision: continue, change one variable, hold, or stop.

## Intelligence gaps required before launch

- Product-level AOV and contribution margin.
- Definition of the current 10% margin and which costs it excludes.
- Product stock and supplier reliability.
- Shipping subsidy and geographic delivery economics.
- Payment-processing costs and settlement delays.
- Refund, cancellation, and chargeback assumptions.
- Current Meta Pixel, Conversions API, analytics, and WooCommerce event quality.
- Hero product and target audience.
- Existing creative assets and landing-page readiness.
- Whether the R$20 daily amount is a one-month seed or a continuing base contribution.

## Final recommendation

**RECOMMENDATION:** Approve the mission conditionally. Begin only after the preflight gate and product economics are verified. Define success in Month 1 as obtaining attributable revenue and a credible repeatability signal while protecting capital; define permission to scale solely as positive settled marketing profit.

**RECOMMENDATION:** If no product can offer enough contribution reais to support a realistic CAC, do not force Meta advertising to solve the problem. Improve margin, raise order value through a coherent bundle, secure supplier support, or use lower-cost acquisition channels before resuming.

**ASSESSMENT:** Zupp1's educational philosophy and system coherence may improve trust and conversion, but the campaign must test whether that behavior produces enough contribution to pay for acquisition. The philosophy remains a guiding hypothesis until the economics are observable.
