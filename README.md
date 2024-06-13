<h1>Mortgage-Backed Security Analysis (Freddie Mac Gold Pool FG B32512)</h1>

<h2>Objective</h2>
To analyze the Mortgage-Backed Security (Freddie Mac Gold Pool FG B32512), this project applies theoretical frameworks from "The Handbook of Fixed Income Securities, Ninth Edition" by Frank J. Fabozzi. Specifically, the analysis focuses on generating interest rate paths, modeling prepayments, calculating cash flows, and estimating the security's value, underpinned by quantitative methods.

<h2>Data & Methodology</h2>

This project provides a comprehensive pricing analysis of Freddie Mac Gold Pool FG B32512, a mortgage-backed security guaranteed by the U.S. government. The approach leverages financial modeling techniques to simulate future interest rate scenarios, predict prepayment behaviors, calculate subsequent cash flows and valuate the security.  

The data was obtained from Bloomberg.  

The Vasicek model is particularly chosen to simulate interest rate paths. The model in particular was favored for its effectiveness in capturing the mean-reverting nature of interest rates, essential for realistic financial forecasting.  

<em>Mathematical representation of the model:</em>

$$
dr_t = \kappa (\theta - r_t) dt + \sigma dW_t
$$

The prepayment dynamics were captured using an adjusted PSA (Public Securities Association) model, calibrated with Bloomberg's CPR data. The model starts with a gradual increase in prepayment rates over the initial 30 months, stabilizing to a constant rate thereafter, reflecting typical borrower behavior influenced by changing economic conditions.

Cash flows for the MBS were computed along each interest rate path using the adjusted PSA model. The formula used integrates both scheduled payments and potential prepayments, thereby offering a comprehensive view of future cash inflows:

$$
\text{Cash Flow}_t = \text{Interest}_t + \text{Scheduled Principal}_t + \text{Prepayment}_t
$$

where each component is derived from the current principal balance, the calculated monthly interest rate, and the SMM rate <em>(from the prepayment model)</em>.

The MBS's value was derived by averaging the present values of anticipated cash flows across all simulated interest rate paths. Discount factors were calculated using the respective path's rates, facilitating an accurate assessment of the security's fair market value.


<h2>Visualization Of Interest Rate Paths</h2>

<p align="center">

<img src="https://i.imgur.com/7KxdWhv.png" height="80%" width="80%" alt="IntR8Paths"/>
<br />
<br />

<h2>Distribution of Discounted Cash Flows</h2>

<p align="center">

<img src="https://i.imgur.com/m22QMSL.png" height="80%" width="80%" alt="DistDiscCF"/>
<br />
<br />

<h2>Conclusion</h2>

The valuation model indicates that the security is overvalued in the market. Given that,  

- Calculated Security Value: $654,907.87
- Market-based Fair Value: $832,988.32

The analysis of Freddie Mac Gold Pool FG B32512 using the Vasicek model and an adjusted PSA prepayment model provides a detailed insight into the pricing mechanisms of MBS. The results affirm that the security is overpriced, reflecting the effectiveness of the chosen model and the reliability of the input data. This project not only enhances the understanding of MBS pricing dynamics but also demonstrates the practical application of advanced financial theories in real-world asset valuation.
