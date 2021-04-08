## Codes for submission to Energy Policy.
The preliminary work was presented at TRB 2021. 
The fulfilled work has been preprinted at [SSRN](https://ssrn.com/abstract=3687504), and it is accepted by Energy Policy.

### Rcode and RMarkDown
We used R to process socioeconomic data including California rebate data from 2010 to 2018, median income data from Census Bureau, and CES3.0 score record from CARB.
The main processing is to compute the Gini index and Suit index inside the data. The detailed codes are included in RCode folder.

### Geoda 

After preliminary processing in R, we feed the rebate, income, CES3.0 score into Geoda to seek the spatial distribution and autocorrelation, quantified by Moran's I statistic.
With well-developed function and tools in Geoda, the processing is not so complicated. The brief steps are summarized as below:
1. Import geoda/tl_2016_06_tract.shp to Geoda
2. Access the ClusterMaps section, select Univariate Local Moran's I (or Bivariate Local Moran's I accordingly).
3. Import dependent varibale as income/CES3.0 score and independent variable as rebate. We have data on varying temporal horizons, e.g., per year, average of before-/after-income-cap policy, and average over years)
4. For recommendation, the metrics that we selected are per-year and before-/after policy ones.

We are happy to help if you have any question. If you used any part of the code, please cite the following paper: 

@article{guo2020disparities,
  title={Disparities and Equity Issues of Electric Vehicles Rebate Allocation},
  author={Guo, Shuocheng and Kontou, Eleftheria},
  journal={Available at SSRN 3687504},
  year={2020}
}
