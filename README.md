# India–FDI Regulatory Heterogeneity Analysis

This project analyzes how similar or different India’s FDI regulatory framework is 
compared to its major investment partners, using the **OECD FDI Regulatory 
Restrictiveness Index (FDIRRI 2023)**. The study computes cross-country 
heterogeneity scores using the **Manhattan distance formula** and visualizes them 
through heatmaps.

---

## Overview
- **Goal:** Quantify India’s regulatory similarity/divergence with FDI partners.  
- **Method:** Compute heterogeneity using the **Manhattan distance (L1 norm)** on OECD’s FDIRRI scores.  
- **Output:** Sector-wise and country-wise **heatmaps** for FDI source and destination partners.  

---

## Sector Focus
The analysis compares restrictiveness across **11 service/tertiary sectors**:
- Retail & Wholesale Trade  
- Transport & Storage  
- Accommodation & Food Services  
- Media & Telecommunications  
- Banking, Insurance & Other Financial Services  
- Professional Services  
- Real Estate Activities  

---

## Methodology
1. **Data Source:** OECD FDIRRI 2023 (scores from 0 = open, 1 = closed).  
2. **Countries:**  
   - *FDI Source Partners*: Mauritius, Singapore, USA, Netherlands, Japan, UK, Germany  
   - *FDI Destination Partners*: Singapore, Mauritius, Netherlands, USA, UK, Switzerland, Mozambique, Australia, Saudi Arabia  
3. **Calculation (Manhattan Distance):**  
   We measure heterogeneity as the average absolute difference across sectoral scores:  

   \[
   Heterogeneity(i,j) = \frac{1}{N} \sum_{k=1}^{N} \big| Score(i,k) – Score(j,k) \big|
   \]  

   where:  
   - \(N\) = number of common sectors  
   - \(Score(i,k)\) = restrictiveness score of country *i* in sector *k*  
4. **Tools:** Python (Pandas, NumPy, Matplotlib, Seaborn, NetworkX).  

---

## Results
### Heatmap 1: India vs FDI Source Partners
- Singapore (0.014) & Mauritius (0.015) → closest to India  
- Japan (0.017) & UK (0.017) → most divergent  
- Source partners among themselves show stronger alignment (0.000–0.005).  

### Heatmap 2: India vs FDI Destination Partners
- Switzerland (0.008) → closest match  
- UK (0.017), Netherlands (0.016), USA (0.016) → most divergent  
- Emerging partners (Mozambique 0.009, Saudi Arabia 0.010) → relatively close to India.  

---

## Key Insights
- **Regulatory isolation:** India remains distinct from both developed and hub economies.  
- **Western convergence:** Developed markets show tight alignment among themselves.  
- **Emerging diversity:** Some developing countries (e.g., Switzerland, Mozambique) align surprisingly close to India.  

---

## Limitations
- OECD coverage excludes key hubs (e.g., UAE, Cyprus).  
- Only regulatory restrictiveness captured (not enforcement/implementation).  
- Static snapshot (2023 data only).  
