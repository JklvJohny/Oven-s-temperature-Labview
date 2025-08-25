# 🔥 Oven Temperature Monitoring & Analysis (LabVIEW)

## Overview
This project simulates an **industrial oven monitoring system** using LabVIEW.  
It allows operators to load oven log files, select a specific oven, and analyze its temperature profile in real time.  
The system highlights **Min, Max, and Mean** values with a graphical gauge indicator for quick operator awareness.

---

## Features
- 📂 **File Loader**: Reads oven log data from `.txt` spreadsheet files (`oven_temperature_sim_15min.txt` included).  
- 📊 **Data Analysis**:
  - Remove timestamps from data array.
  - Compute **Minimum**, **Maximum**, and **Mean** temperature for the selected oven.
- 🎛️ **Interactive Controls**:
  - Choose oven index (`0, 1, 2 …`).
  - Numeric indicators for **Min, Max, Mean**.
  - Gauge bar with **fire icons** for visualization.
- 🖥 **Front Panel**:
  - File Path selector.
  - Gauge with min/mean/max overlay.
  - Indicators for easy operator reading.
- 🔧 **Block Diagram**:
  - Uses `Delete From Array`, `Index Array`, `Array Max & Min`, and `Mean.vi`.
  - Outputs values to both numeric indicators and gauge.

---

## File Structure
- **Collect_data.vi** → Reads and prepares oven data from file.  
- **Min_max_average.vi** → Computes Min, Max, and Mean values for selected oven.  
- **Temperature_gauge.vi** → Displays oven temperature on a vertical gauge with fire icons.  
- **Oven_tem_project.lvproj** → LabVIEW project file.  
- **oven_temperature_sim_15min.txt** → Sample dataset with 4 ovens over 15 minutes (1 Hz sampling).  

---

## Usage
1. Open `Oven_tem_project.lvproj` in LabVIEW.  
2. Run `Collect_data.vi` or directly open `Min_max_average.vi`.  
3. Browse and select `oven_temperature_sim_15min.txt`.  
4. Enter the oven index (e.g., `0 = Oven1`, `1 = Oven2`).  
5. View results:
   - **Gauge bar** shows oven’s temperature profile.  
   - **Numeric indicators** display min, max, mean values.  

---

## Example Dataset
`oven_temperature_sim_15min.txt` contains:
- **Timestamps** (1-second interval).  
- **4 ovens’ temperatures** with realistic fluctuations.  
- An overheating episode on Oven 3 (>250 °C).  

---

## Expected Outcome
- Operators can load log files and visualize oven performance.  
- If temperature exceeds threshold, the gauge highlights the overheating.  
- Min/Max/Mean values are displayed for monitoring and quality control.

---

## Requirements
- LabVIEW 2020 or later (works on LabVIEW 2015+ with minor adjustments).  
- NI standard libraries (File I/O, Array, Statistics).  

---

## Author
Created as part of an **Industrial LabVIEW Simulation Project** for oven monitoring in a food processing factory.
