# ntp_heat_wave_loads
This repository houses the raw data and processing scripts to create the hourly load time series by 
Balancing Authority for the NTP project. Data are scaled to match the 2035 annual total loads data by BA. 
The future loads for different weather years are based on the Total ELectricity Loads (TELL) model.

## Input Files
The input data needed to recreate this process is stored in the [data](data/) directory.

## Output Files
The output of this processing is stored in the [data](data/) directory with the filename 
"TELL_Loads_2035_Based_on_YYYY_Weather.csv".

## Citations
Any use of this data in a publication, presentation, or report should use the following citations. Please contact 
Casey Burleyson (casey.burleyson@pnnl.gov) prior to any reuse of the data.
>
**Citation for the TELL model**
>
McGrath et al., (2022). tell: a Python package to model future total electricity loads in the United States. Journal of Open Source Software, 7(79), 4472, https://doi.org/10.21105/joss.04472
> 
**Citation for the underlying weather data**
>
Burleyson, C., Thurber, T., & Vernon, C. (2023). Projections of Hourly Meteorology by Balancing Authority Based on the IM3/HyperFACETS Thermodynamic Global Warming (TGW) Simulations (v1.0.0) [Data set]. MSD-LIVE Data Repository. https://doi.org/10.57931/1960530
>
Jones, A. D., Rastogi, D., Vahmani, P., Stansfield, A., Reed, K., Thurber, T., Ullrich, P., & Rice, J. S. (2022). IM3/HyperFACETS Thermodynamic Global Warming (TGW) Simulation Datasets (v1.0.0) [Data set]. MSD-LIVE Data Repository. https://doi.org/10.57931/1885756

## Notes
1) Loads in CISO, IPCO, NEVP, and PACE are modeled as a whole in TELL but are separated in GridView. To create the data
for these BAs I used the whole load simulated by TELL and distributed it to the subregions within the BA using the 
annual total load in each subregion to portion out the TELL loads.

## BAs in the WECC 
>
🟢 = Matched with no issue  
🟡 = Caution advised  
🔴 = No match
>
| GV BA | TELL BA | Matched? | Notes |
| :-: | :-: | :-: | :-: |
| AVA | AVA | 🟢 | - |
| AZPS | AZPS | 🟢 | - |
| BANC | BANC | 🟢 | - |
| BPAT | BPAT | 🟢 | - |
| CHPD| CHPD| 🟢 | - |
| CIPB | CISO | 🟡 | Subregion of CISO |
| CIPV | CISO | 🟡 | Subregion of CISO |
| CISC | CISO | 🟡 | Subregion of CISO |
| CISD | CISO | 🟡 | Subregion of CISO |
| DOPD | DOPD | 🟢 | - |
| EPE | EPE | 🟢 | - |
| GCPD | GCPD | 🟢 | - |
| IID | IID | 🟢 | - |
| IPFE | IPCO | 🟡 | Subregion of IPCO |
| IPMV | IPCO | 🟡 | Subregion of IPCO |
| IPTV | IPCO | 🟡 | Subregion of IPCO |
| LDWP | LDWP | 🟢 | - |
| NEVP | NEVP | 🟡 | Subregion of NEVP |
| NWMT | MWMT | 🟢 | - |
| PACW | PACW | 🟢 | - |
| PAID | PACE | 🟡 | Subregion of PACE |
| PAUT | PACE | 🟡 | Subregion of PACE |
| PAWY | PACE | 🟡 | Subregion of PACE |
| PGE | PGE | 🟢 | - |
| PNM | PNM | 🟢 | - |
| PSCO | PSCO | 🟢 | - |
| PSEI | PSEI | 🟢 | - |
| SCL | SCL | 🟢 | - |
| SPCC | NEVP | 🟡 | Subregion of NEVP |
| SRP | SRP | 🟢 | - |
| TEPC | TEPC | 🟢 | - |
| TIDC | TIDC | 🟢 | - |
| TPWR | TPWR | 🟢 | - |
| VEA | CISO | 🟡 | Subregion of CISO |
| WACM | WACM | 🟢 | - |
| WALC | WALC | 🟢 | - |
| WAUW | WAUW | 🟢 | - |
