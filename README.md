# Experimental Results for Soil Moisture Sensing
Our experiment investigates the relationship between key agricultural soil parameters—specifically soil moisture, Time of Flight (ToF), and Received Signal Strength Indicator (RSSI). To conduct this study, we collected soil samples representative of typical agricultural conditions. Due to their initial humidity levels, these samples were subjected to a two-day drying process under sunlight to achieve a stable baseline for evaluation. Soil moisture content is expressed as Volumetric Water Content (VWC), a crucial metric for assessing the amount of water retained within the soil matrix. Understanding these relationships helps in optimizing irrigation strategies and improving agricultural efficiency.
# Table of Contents
-[Experiment Setup](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/blob/main/README.md#experiment-setup)
-[Setting Up](## Setting Up)
  *[Environment Setup](### Environment Setup)
  *[Data Collection Setup](### Data Collection Setup)
-[Dataset Description](## Dataset Description)
-[Processing and Analysis](## Processing and Analysis)
-[Credits](## Credits)
## Experiment Setup
To systematically collect soil moisture data, we conducted measurements over a one-month period, averaging readings taken every **30 seconds** into single data points. For this purpose, we deployed three moisture sensors, each placed in a separate **50-liter container** filled with soil sourced from the front lawn of **IIT Kanpur K.D Building**. Each sensor was positioned at varying depths within its respective container to account for spatial variations in moisture distribution.The **Arduino Uno** was used to record **Volumetric Water Content (VWC)**, ensuring accurate and consistent moisture readings.
Additionally, we integrated the **DWM1001 module** into our experiment to monitor **RSSI** and **ToF** variations. The module was strategically placed at both ends of a 50-liter bucket filled with soil, simulating real-world conditions. This setup enabled us to analyze the relationship between soil moisture content and radio wave propagation. By positioning the DWM1001 modules at opposite ends of the soil-filled bucket, we could effectively measure signal fluctuations in response to changes in moisture levels, providing valuable insights into the interaction between soil properties and wireless signal transmission.
![Full setup](/setup-images/All_image.png)
## Setting Up
### Environment Setup
To ensure a smooth and consistent development experience, we have included an env folder in this repository. To activate the environment in **Linux Systems** use
~~~
source env/bin/actiavte
~~~
Then start the **Jupyter-Notebook** in browser using command
~~~
jupyter notebook
~~~
### Data Collection Setup
For **Moisture Sensor** data collection using **Arduino Uno** we have a jupyter file in [Data_Collection_Arduino](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/blob/main/dataset-collection/Arduino_data_collection.ipynb). You need to connect the Arduino with Moisture Sensor in any com port (we have used COM PORT 7).

For **RSSI** and **TOF** data collection we require a **DWM1001** module. We also require flasher to flash the [initiator](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/tree/main/dataset-collection/initiator) and [responder](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/tree/main/dataset-collection/responder) to DWM1001 module. Use link [**J-link Flasher**](https://www.segger.com/products/debug-probes/j-link/technology/flash-download/) to download and flash to the module. Use a *Raspberry Pi* to record the RSSI and TOF data.

## Dataset Description
Data collection was conducted over a **30-day period**, with measurements taken every **30 seconds**. This high-frequency data acquisition allowed us to capture detailed temporal variations and potential correlations between soil moisture, ToF, and RSSI.
The collected [**dataset**](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/tree/main/dataset) is stored in the dataset folder and comprises two files:

- [**mois_data.csv**](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/blob/main/dataset/mois_data.csv): Contains VWC data recorded at 30-second intervals. The data is generated using an Arduino-based setup.

- [**tof_rssi.csv**](https://github.com/BKS2280/Soil-Moisture-Sensing-Experimental-Dataset/blob/main/dataset/tof_rssi.csv): Contains ToF and RSSI measurements collected from the DWM1001 UWB sensor module.
This dataset serves as the foundation for analyzing how soil moisture levels correlate with ToF and RSSI values.

## Processing and Analysis
In the 'data-analysis' folder, we use a Jupyter Notebook to analyze and visualize sensor data. To use it:

  -Set Dataset Path: Update the dataset path in the notebook to match your local file location.

  -Part 1: Temporal Variation: Plots TOF, RSSI, and VWC over time for each moisture sensor.
  ![Moisture Sensor 1](/data-processing-plots/temporal_sensor_1.jpg)

  -Part 2: Correlation Analysis: Examines the relationship between VWC and TOF for Moisture Sensor 1 using scatter plots and correlation coefficients.
  ![Moisture Sensor 1](/data-processing-plots/scatter_plot_vwc_tof_1.jpeg)

## Credits
Contributors whose support and expertise have been invaluable in the development of CosmicDance:
-[Amitangshu Pal](https://www.cse.iitk.ac.in/users/amitangshu/)
  
