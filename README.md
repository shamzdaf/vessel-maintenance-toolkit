# Naval Vessel Maintenance Toolkit

**A Python-based toolkit for preventive/corrective maintenance, diagnostics, and machining workflows for naval vessels.**

This repository is inspired by the **Intern Maintenance Engineer** role at **Nigerian Navy Fleet Support Group (FSG) West - Lagos**, where the focus was on:

- **Preventive and corrective maintenance** of naval vessels (e.g., NNS MIRA, NNS Centenary).
- **Diagnostics** of mechanical, electrical, and hydraulic systems.
- **Machining and fabrication** (milling, lathe, welding) for component refurbishment.
- **Sea-trial safety procedures** (pre-start checks, bridge controls, compliance).

---

##  **Purpose**

This toolkit aims to:  
✅ **Improve propulsion efficiency** through optimized maintenance schedules.  
✅ **Accelerate fault identification** with structured diagnostics.  
✅ **Automate machining workflows** (e.g., shaft/gear precision calculations).  
✅ **Ensure safety compliance** with pre-start checklists and monitoring tools.

---

##  **Features**


| **Module**              | **Description**                                                                   | **Key Functions**                                        |
| ----------------------- | --------------------------------------------------------------------------------- | -------------------------------------------------------- |
| `propulsion_optimizer`  | Optimizes propeller shaft alignment and compressor performance for naval vessels. | `align_shaft()`, `check_compressor_efficiency()`         |
| `diagnostics_tool`      | Diagnoses faults in mechanical, electrical, and hydraulic systems.                | `identify_fault()`, `generate_diagnostic_report()`       |
| `machining_calculator`  | Calculates precision parameters for milling, lathe, and welding operations.       | `calculate_milling_params()`, `welding_strength_check()` |
| `safety_compliance`     | Validates pre-start checks and sea-trial safety protocols.                        | `pre_start_checklist()`, `monitor_bridge_controls()`     |
| `maintenance_scheduler` | Schedules preventive/corrective maintenance to reduce unplanned downtime.         | `schedule_maintenance()`, `predict_downtime()`           |


---

## **Repository Structure**

```
vessel-maintenance-toolkit/
├── scripts/
│   ├── propulsion_optimizer.py   # Propulsion efficiency tools
│   ├── diagnostics_tool.py       # Fault diagnostics for vessel systems
│   ├── machining_calculator.py   # Precision machining calculations
│   ├── safety_compliance.py      # Safety protocol validation
│   └── maintenance_scheduler.py  # Maintenance planning and downtime prediction
├── README.md                     # Project documentation
├── requirements.txt               # Python dependencies
└── LICENSE                        # MIT License
```

---

##  **Installation**

### **Prerequisites**

- Python 3.8+
- Required libraries: `pandas`, `numpy`, `scipy`

### **Setup**

1. Clone the repository:
  ```bash
   git clone https://github.com/shamzdaf/vessel-maintenance-toolkit.git
   cd vessel-maintenance-toolkit
  ```
2. Install dependencies:
  ```bash
   pip install -r requirements.txt
  ```

---

##  **Quick Start**

### **1. Propulsion Optimization**

Optimize propeller shaft alignment and compressor efficiency:

```python
from scripts.propulsion_optimizer import PropulsionOptimizer

# Initialize with vessel data
optimizer = PropulsionOptimizer("data/vessel_data.csv")

# Check shaft alignment for NNS MIRA
alignment_status = optimizer.align_shaft(vessel="NNS MIRA", tolerance=0.05)
print(f"Shaft alignment status: {alignment_status}")

# Check compressor efficiency for NNS Centenary
compressor_efficiency = optimizer.check_compressor_efficiency(vessel="NNS Centenary")
print(f"Compressor efficiency: {compressor_efficiency}%")
```

### **2. Diagnostics Tool**

Diagnose faults in vessel systems:

```python
from scripts.diagnostics_tool import DiagnosticsTool

diagnostic = DiagnosticsTool()

# Identify fault in hydraulic system
fault = diagnostic.identify_fault(
    system="hydraulic",
    symptoms=["low_pressure", "leakage"]
)
print(f"Potential fault: {fault}")

# Generate a diagnostic report
report = diagnostic.generate_diagnostic_report(
    vessel="NNS MIRA",
    system="propulsion",
    fault="misaligned_shaft",
    recommendations=["Realign propeller shaft", "Check bearing wear"]
)
print(report)
```

### **3. Machining Calculator**

Calculate precision parameters for machining operations:

```python
from scripts.machining_calculator import MachiningCalculator

calculator = MachiningCalculator()

# Calculate milling parameters for a helical gear
milling_params = calculator.calculate_milling_params(
    material="steel",
    diameter=50,
    depth=5
)
print(f"Milling parameters: {milling_params}")

# Check welding strength for a structural fitting
welding_strength = calculator.welding_strength_check(
    material="steel",
    thickness=10,
    weld_type="arc"
)
print(f"Welding strength: {welding_strength} MPa")
```

### **4. Safety Compliance**

Validate pre-start checks and sea-trial protocols:

```python
from scripts.safety_compliance import SafetyCompliance

safety = SafetyCompliance()

# Run pre-start checklist for NNS Centenary
checklist_status = safety.pre_start_checklist(vessel="NNS Centenary")
print(f"Pre-start checklist status: {checklist_status}")

# Monitor bridge controls during sea trial
bridge_status = safety.monitor_bridge_controls(vessel="NNS MIRA")
print(f"Bridge controls status: {bridge_status}")
```

### **5. Maintenance Scheduler**

Schedule preventive/corrective maintenance:

```python
from scripts.maintenance_scheduler import MaintenanceScheduler

scheduler = MaintenanceScheduler()

# Schedule maintenance for NNS MIRA
schedule = scheduler.schedule_maintenance(
    vessel="NNS MIRA",
    component="propeller_shaft",
    interval=30  # days
)
print(f"Next maintenance due: {schedule['next_due']}")

# Predict downtime for compressor replacement
downtime = scheduler.predict_downtime(
    task="compressor_replacement",
    vessel="NNS Centenary"
)
print(f"Estimated downtime: {downtime} hours")
```

---

##  **Example Data**

### `**data/vessel_data.csv**`

```csv
vessel,component,parameter,value,timestamp
NNS MIRA,propeller_shaft,alignment,0.02,2023-05-01 08:00
NNS MIRA,compressor,efficiency,85,2023-05-01 08:00
NNS Centenary,propeller_shaft,alignment,0.08,2023-05-01 08:00
NNS Centenary,compressor,efficiency,78,2023-05-01 08:00
```

### `**data/machining_params.json**`

```json
{
  "milling": {
    "steel": {
      "speed": 1200,
      "feed_rate": 0.5,
      "depth_of_cut": 2.0
    }
  },
  "welding": {
    "arc": {
      "steel": {
        "current": 150,
        "voltage": 25,
        "strength": 400
      }
    }
  }
}
```

### `**data/safety_checklists.json**`

```json
{
  "pre_start": [
    "Check engine oil levels",
    "Inspect propeller shaft alignment",
    "Test hydraulic system pressure",
    "Verify bridge controls"
  ],
  "sea_trial": [
    "Monitor engine temperature",
    "Check navigation systems",
    "Validate communication equipment"
  ]
}
```

---

##  **Use Cases**


| **Scenario**                       | **Tool**                   | **Output**                  |
| ---------------------------------- | -------------------------- | --------------------------- |
| Optimize propeller shaft alignment | `propulsion_optimizer.py`  | Alignment status (Boolean)  |
| Diagnose hydraulic system faults   | `diagnostics_tool.py`      | Fault report (Markdown)     |
| Calculate milling parameters       | `machining_calculator.py`  | Machining parameters (JSON) |
| Validate pre-start checklist       | `safety_compliance.py`     | Checklist status (Boolean)  |
| Schedule compressor maintenance    | `maintenance_scheduler.py` | Maintenance schedule (JSON) |


---

##  **Customization**

### **Extend the Toolkit**

- **Add more vessels**: Update `vessel_data.csv` with additional naval vessels.
- **Improve diagnostics**: Integrate **machine learning** (e.g., `scikit-learn`) for fault prediction.
- **Add CAD integration**: Use `python-OCC` or `FreeCAD` for 3D modeling of components.
- **IoT Integration**: Fetch live data from vessel sensors using `pymodbus` or `opcua`.

### **Visualization (Optional)**

Add a **Streamlit dashboard** to visualize:

- Propulsion efficiency trends.
- Maintenance schedules.
- Machining parameter comparisons.

Example:

```python
# Install Streamlit: pip install streamlit
import streamlit as st
import pandas as pd

st.title("Naval Vessel Maintenance Dashboard")
df = pd.read_csv("data/vessel_data.csv")
st.line_chart(df, x="timestamp", y="value", color="component")
```

---

##  **License**

This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.
ir guidance.
