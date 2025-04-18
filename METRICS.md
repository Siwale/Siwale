# How I Calculate Impact Metrics  

## Claim: "75% Reduction in Unauthorized Access"  
**Data Source**:  
- Riverside Farm’s access logs (2021 vs 2022).  

**Methodology**:  
1. Calculated daily unauthorized entry attempts pre-system (2021 avg: 12.7/day).  
2. Post-implementation (2022 avg: 3.1/day).  
3. **Formula**: ((12.7 - 3.1) / 12.7) * 100 = 75.6%  

**Edge Cases**:  
- Excluded days with power outages (system offline).  

Raw Data: [CSV](docs/metrics/riverside-access-2021-2022.csv)  