# Risk Assessment Fundamentals

## Qualitative Risk Assessment
- Evaluates risks using subjective criteria and broad categories
- Visualized using methods like traffic light grids:
  - **Red**: High risk
  - **Yellow**: Medium risk
  - **Green**: Low risk

### Example Assessment:
| Risk Factor             | Impact  | Annualized Rate | Cost of Controls | Overall Risk |
|-------------------------|---------|-----------------|------------------|-------------|
| Legacy Windows Clients  | Medium  | High (🔴)       | Medium           | High (🔴)   |
| Untrained Staff         | Low     | Medium          | Low              | Medium (🟡) |
| No Anti-Virus Software  | Medium  | High (🔴)       | Medium           | High (🔴)   |

## Quantitative Risk Assessment
Uses numerical values to calculate risk exposure:

### Key Formulas:
- **SLE (Single Loss Expectancy)** = Asset Value (AV) × Exposure Factor (EF)  
  *Example: $1,000 laptop × 1.0 EF = $1,000 SLE*
- **ALE (Annualized Loss Expectancy)** = ARO × SLE  
  *Example: 7 thefts/year × $1,000 SLE = $7,000 ALE*

### Core Components:
- **ARO (Annualized Rate of Occurrence)**: 
  How often an event occurs yearly (e.g., hurricane likelihood in Florida vs. Montana)
- **Asset Value (AV)**: 
  Total value including replacement cost, lost sales, fines
- **Exposure Factor (EF)**: 
  Percentage of value lost (0.25 for 25% loss, 1.0 for total loss)

## Impact Categories
1. **Life**: Human safety (highest priority)
2. **Property**: Physical assets and infrastructure
3. **Safety**: Environmental danger levels
4. **Finance**: Monetary consequences

## Likelihood vs. Probability
| Concept        | Type         | Description                          | Examples                     |
|----------------|--------------|--------------------------------------|------------------------------|
| **Likelihood** | Qualitative  | Subjective measurement               | Rare, Possible, Almost Certain |
| **Probability**| Quantitative | Statistical measurement              | 10% chance, 1-in-100 odds    |

### Risk Matrix Example:
| Likelihood       | Moderate | Major    | Catastrophic |
|------------------|----------|----------|--------------|
| **Almost Certain**| High     | Extreme  | Extreme      |
| **Likely**       | Moderate | High     | Extreme      |
| **Possible**     | Low      | Moderate | High         |
| **Unlikely**     | Low      | Low      | Moderate     |
| **Rare**         | Low      | Low      | Low          |

## Risk Appetite vs. Tolerance
- **Risk Appetite**: 
  Broad acceptable risk level (e.g., highway speed limit = 55 mph)
- **Risk Tolerance**: 
  Acceptable variance from appetite (e.g., ticketing only at 65+ mph)
- **Factors influencing tolerance**: Conditions, context, severity

## Risk Register
Documents project-specific risks with:
- **Key Risk Indicators** (e.g., undefined project requirements)
- **Risk Owners**: Individuals responsible for managing risks
- **Risk Threshold**: Point where mitigation cost = value gained
