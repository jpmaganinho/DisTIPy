# DisTIPy

---

# **Table of Contents**

1. Introduction
2. Installation & requirements
3. Fitting methodology description
4. Interface utilization guidelines
   
      4.1. Measurement information section
   
      4.2. Magnetoconductivity fitting section
   
      4.3. Graphical visualization section
   
      4.4. Export results section
5. References

---

# **1. Introduction**

DisTIPy is a magnetoconductivity fitting software designed to disentangle the competing transport mechanisms in Disordered 3D Topological Insulator (TI) systems (and beyond). It implements a structured three-stage fitting workflow that progressively incorporates contributions typically observed in TI magnetotransport:

1. Weak anti-localization (WAL) effects;
2. A quadratic in-field scattering contribution;
3. Linear Magnetoresistance (LMR) effects.

At each stage, the software returns optimal-fit parameters, uncertainties, and fit quality metrics, enabling users to compare the temperature dependence, stability and statistical performance of each model. The appropriate magnetoconductivity model must then be selected based on the physical consistency and temperature trend of the fitted parameters (see Ref. [REF letter] for an example analysis).

This release is designed for magneto-resistance measurements, using a 4-point probe technique, conducted with the Physical Properties Measurement System (PPMS) from Quantum Design, on samples exhibiting WAL features across the whole temperature range. Under these conditions, DisTIPy’s sequential modeling approach provides a reliable framework for identifying the dominant transport mechanisms in disordered 3D TIs.

---

# **2. Installation & requirements**

Fazer só no final quando colocar no git e tiver o executável

---

# **3. Fitting methodology description**

For a full description and physical justification of the fitting methodology used in DisTIPy, please refer to Ref. [REF letter].

---

# **4. Interface utilization guidelines**

DisTIPy’s interface is organized into two main panels. The left panel contains three sections:

* Measurement information section, for loading and describing the input data;
* Magnetoconductivity fitting section, for processing the data and executing each stage fits;
* Export results section, for saving processed data and fit outputs.

In the right panel users can display and save the experimental magnetoconductivity curves and the corresponding fit results.

The following sections are structured according to typical workflow and provide detailed guidance for using each part of the interface effectively.

---

## **4.1. Measurement information section**

Begin by entering the sample’s physical dimensions – length, width, and thickness – as well as the spacing between the voltage probes. Accurate values are essential for converting the measured resistance data into 2D conductivity.

Next, in the **Data info** block, select the folder containing the temperature-dependent magnetotransport dataset, and specify the PPMS puck measurement channel.

---

## **4.2. Magnetoconductivity fitting section**

Before proceeding with the fitting framework, enter the filter window size, which sets the number of next neighboring points used in the moving-average smoothing to the 2D magnetoconductivity. Afterwards, perform the preprocessing and fitting steps sequentially using the corresponding buttons. A progress bar indicates the completion of each stage.

---

## **4.3. Graphical visualization section**

After performing the magnetoconductivity fitting, three graphical visualization options are available via the **“Choose option”** button:

* **Temperature-dependent 2D magnetoconductivity**: displays raw and filtered 2D magnetoconductivity for all measured temperature.
* **2D Magnetoconductivity for a specific temperature**: compares the experimental magnetoconductivity data with the three fitted models at the temperature selected with the **“Choose temperature”** button.
* **Model-dependent fitting parameters temperature evolution**: shows the temperature dependence of the fitted parameters and associated metrics for each model, enabling evaluation of their physical consistency and temperature evolution. These plots are essential for selecting the most appropriate model and identifying the dominant transport mechanisms in the sample.

The toolbar at the bottom allows zooming into regions of interest and saving the generated figures.

---

## **4.4. Export results section**

In this section, the data and fitting results can be exported to .csv files.

* For the temperature selected with the **“Choose temperature”** button, the raw and filtered magnetoconductivity data and the fitted model curves can be saved using the **“Save Magnetoconductivity Data + Fits”** button.
* For the model selected with the **“Choose model”** button, the fitting parameters and associated metrics across all temperatures can be exported using the **“Save fitting parameters VS T”** button.

---

# **5. References**



