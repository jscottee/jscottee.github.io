#### Reach me on LinkedIn → [James Scott | LinkedIn](https://www.linkedin.com/in/jscottee)

# R&D Test / Reliability Engineer
*This portfolio presents selected engineering projects focused on reliability testing, experimental validation, and data-driven failure investigation of electromechanical systems.*

## Project: Early-Stage Reliability & Testability Planning for a Multimodal Electromechanical System
**Role:** Electrical Engineer (Astral AR)
### Context
Astral AR is an early-stage effort exploring a multimodal electromechanical sensing concept. At the time of my involvement, the system was in the conceptual and feasibility phase, with limited hardware implementation and limited field data available.

The primary objective was to reason about system structure, interfaces, and observability early enough to avoid downstream reliability and integration issues.

### My Role

- Contributed to **system decomposition** and interface definition across electrical, sensing, and mechanical subsystems
- Focused on **testability, observability, and reliability risk identification** rather than execution of validation testing
- Produced **hardware and subsystem block diagrams** to support future test planning and integration
- Documented assumptions, open risks, and candidate validation approaches for downstream development

### Technical Challenges

- No mature hardware or field failures to analyze
- High uncertainty around timing behavior, environmental sensitivity, and cross-subsystem interactions
- Need to reason about **potential reliability risks without empirical data**

To ensure early system concepts were testable and verifiable, I approached the Astral architecture with explicit attention to measurement observability and verification boundaries. The diagram below illustrates the end-to-end data flow from physical stimuli through sensing, timing, control, logging, and offline analysis, with each stage designed to support incremental validation, traceability, and root-cause isolation rather than treating testing as a post-integration activity.

<div align="center">
  <img src="/assets/System-Level Signal-Flow Diagram.png"
       width="900">
  
  <p><em>
  High-level signal flow diagram for RF/imaging system architecture.
  </em></p>
</div>

### Approach

- Performed **early-stage reliability risk identification** by analyzing signal paths, power dependencies, and interface boundaries
- Evaluated where **timing drift, environmental sensitivity, or observability gaps** were likely to emerge once hardware existed
- Assessed which risks would be testable with instrumentation versus those requiring architectural mitigation
- Framed candidate validation strategies without implying execution or closure

### Outcomes

- Clear documentation of **reliability-relevant risks and assumptions**
- Testability-informed subsystem diagrams suitable for future DVT and characterization work
- A structured foundation enabling downstream engineers to design validation tests with fewer blind spots

---

## Project: Reliability Characterization and Root Cause Analysis of Optical Test Systems
**Role:** Electro-Optical Engineer (E Ink)
### Context

This project focused on evaluating the **stability and reliability of optical test systems** used for precision measurement. Reliability, repeatability, and long-term drift directly impacted calibration confidence and qualification decisions.

### My Role

- Designed and implemented **automated optical and electromechanical test systems** using Python, MATLAB, and C
- Built **data-acquisition pipelines** coordinating imaging hardware, timing signals, and environmental controls
- Planned and executed **environmental and long-duration stability tests**
- Performed **hands-on root cause analysis (RCA)** using instrumentation-driven experiments
- Communicated findings to engineering teams to inform design and qualification decisions

### Technical Challenges

- Performance drift emerging only over extended runtimes
- Ambiguity between **true hardware degradation** and **measurement noise**
- Timing and synchronization interactions across hardware and software boundaries
- Maintaining repeatability under varying environmental conditions

<div align="center">
  <img src="/assets/camera_pixel_response_linearity_overlaid.png"
       alt="Camera pixel response linearity (pre-calibration)"
       width="500">
  
  <p><em>
  Illustrative pre-calibration camera response used in E Ink panel testing, highlighting nonlinearity and sensitivity to low-light reference stability.
  </em></p>
</div>

### Measurement Model and Calibration Implications

- Pre-calibration camera response was nonlinear across lightness, with low-light behavior dominated by offset, noise floor, and system stability limits.
- Drift mechanisms were decomposed into illumination/optics, sensor response, timing/synchronization, and environmental coupling to avoid misattributing panel behavior.
- Calibration and control strategies were evaluated based on repeatability impact and operational practicality (long-duration runs, environmental setpoints, re-baselining cadence).

### Approach

- Designed controlled experiments to isolate timing, environmental, and hardware contributors
- Used oscilloscopes, logic analyzers, and signal generators to investigate synchronization and drift behavior
- Conducted a **spectroscopic gage study** to quantify sources of measurement variability
- Compared results across conditions to distinguish degradation mechanisms from instrumentation effects

### Outcomes

- Identified dominant contributors to drift and instability
- Separated true degradation from measurement noise with quantified uncertainty
- Delivered **data-backed recommendations** for calibration procedures and environmental controls
- Improved repeatability and confidence in qualification and validation decisions

---

## Subsystem Validation and Integration Debugging (Urbx)
**Role:** Test / Integration Engineer (Urbx)

### Context  
Subsystem-level validation and integration support for electromechanical assemblies, focused on rapid debug, fault isolation, and corrective action in a cross-functional environment.


- Executed subsystem-level validation of electromechanical assemblies including motor-control electronics and sensor interfaces
- Performed root cause analysis of timing and integration failures using targeted test scripts and bench instrumentation
- Supported defect documentation and corrective action development in collaboration with cross-functional teams
