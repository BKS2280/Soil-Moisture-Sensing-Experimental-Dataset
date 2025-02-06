# Experimental Results for Soil Moisture Sensing
Our experiment investigates the relationship between key agricultural soil parameters—specifically soil moisture, Time of Flight (ToF), and Received Signal Strength Indicator (RSSI). To conduct this study, we collected soil samples representative of typical agricultural conditions. Due to their initial humidity levels, these samples were subjected to a two-day drying process under sunlight to achieve a stable baseline for evaluation. Soil moisture content is expressed as Volumetric Water Content (VWC), a crucial metric for assessing the amount of water retained within the soil matrix. Understanding these relationships helps in optimizing irrigation strategies and improving agricultural efficiency.
## Dataset Description
Data collection was conducted over a 30-day period, with measurements taken every 30 seconds. This high-frequency data acquisition allowed us to capture detailed temporal variations and potential correlations between soil moisture, ToF, and RSSI.

The collected [dataset](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/tree/main/dataset) is stored in the dataset folder and comprises two files:

> [mois_data.csv](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/blob/main/dataset/mois_data.csv): Contains VWC data recorded at 30-second intervals. The data is generated using an Arduino-based setup.

> [tof_rssi.csv](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/blob/main/dataset/tof_rssi.csv): Contains ToF and RSSI measurements collected from the DWM1001 UWB sensor module.

This dataset serves as the foundation for analyzing how soil moisture levels correlate with ToF and RSSI values.
