# EPRA Reference Data – FairPower: EquiTariff Simulator

This file summarizes key statistics from the **EPRA Biannual Energy & Petroleum Statistics Report (H1 2025/2026)**.  
It provides official benchmarks to ground FairPower's AI models, clustering, and policy narrative.

---

## 📊 Demand & Supply Benchmarks
- Electricity demand growth: **+8.25%** (July–Dec 2025)
- Peak demand: **2,439.06 MW** (Dec 3, 2025)
- Installed capacity mix:
  - Geothermal: **25.72%**
  - Hydro: **23.78%**
  - Solar: **14.74%**
  - Wind: **11.89%**
  - Thermal: **17.12%**
- Renewable share of supply: **78.79%**

---

## 🏠 Consumption by Region
- Nairobi region: **44.24%** (2,627.44 GWh)
- Coast region: **16.46%** (977.90 GWh)
- North Eastern: **11.23%** (666.98 GWh)
- Central Rift: **9.33%** (553.74 GWh)
- Mt. Kenya: **6.56%** (389.52 GWh)
- West Kenya: **5.43%** (322.89 GWh)
- North Rift: **4.66%** (276.69 GWh)
- South Nyanza: **2.07%** (123.38 GWh)

---

## 👥 Consumption by Category
- Industrial: **49.25%** (2,924.48 GWh) – first time below 50%
- Domestic: **32.93%** (1,955.77 GWh)
- Small Commercial (SME): **16.63%** (987.51 GWh)
- Street Lighting: **1.12%** (66.41 GWh)
- Electric Mobility: **0.08%** (4.57 GWh, +152.5% growth)

---

## 💡 Policy Hooks
- **Fairness Benchmark**: KSh **971M** saved by ToU tariff beneficiaries.
- **FERFA volatility**: KSh **1.77/kWh** (Jul 2025) → KSh **0.68/kWh** (Dec 2025).
- **Energy Burden Standard**: 10% of income → households above flagged by simulator.
- **Misclassification Risk**: ~15% of households paying 20% more.

---

## 🚀 Hackathon Narrative Anchors
- **Green Equity Story**: 78.8% renewable dominance → stable, low-cost tariffs for Segment A.
- **Future-Proofing**: +152.5% growth in e-mobility → Segment D as early adopters, potential cross-subsidy lever.
- **Reliability vs Affordability**: Avg monthly outage duration **8.39 hours** → quality-adjusted tariffs for vulnerable households.

---

## ✅ Usage in FairPower
- Joel: Use demand growth, regional weights, and category proportions in clustering (`feature/data-prep`, `feature/clustering-engine`).
- Juliet: Use fairness benchmark, renewable dominance, and e-mobility growth in policy pitch.
- Team: Align synthetic dataset proportions with EPRA benchmarks for credibility.

---

## 📁 Data Sources Available

### CSV Datasets
1. **Households_2019.csv** (44 KB)
   - County and subcounty household counts
   - Average household sizes
   - Base year: 2019

2. **Chapter-9-Energy-Tables.csv** (4.4 KB)
   - Physical energy use by industry sector
   - Energy flows and natural inputs
   - Solar, biomass, and other energy sources

3. **Average_Electricity_Yield.csv** (2.8 KB)
   - Historical tariff yields by customer category (Domestic, SME, Industrial)
   - Time series: 2018-2021+
   - Unit: KSh/kWh

4. **API_EG.ELC.ACCS.ZS_DS2_en_csv_v2_158.csv** (671 bytes)
   - Electricity access statistics
   - World Bank data format

### Reference Documents
- **Biannual Statistics Report 2025-2026_0.pdf** (1.9 MB)
  - Official EPRA half-year report (H1 2025/2026)
  - Source for all benchmarks above

### Mapping Files
- **subcounty_to_county_mapping.json** / **.pkl**
  - Validated: 47 counties, 333 subcounties
  - Critical for aggregating subcounty-level data to county totals
