# AdaptiveCopilot

AdaptiveCoPilot: Design and Testing of a NeuroAdaptive LLM Cockpit Guidance System in both Novice and Expert Pilots

# System Design

![Figure 1: Apparatus](images/figure1_apparatus.jpg)

**Figure 1. Apparatus**  
Shows a participant performing a trial.

1. The Quest 3 headset
2. The experiment display for monitoring
3. The fNIRS device
4. The system computer

---

![Figure 2: Experiment Condition](images/figure2_experiment_condition.png)

**Figure 2. Experiment Condition**  
Illustrates the three conditions in our evaluation study.

---

![Figure 3: False Error Rates](images/figure3_false_error_rates.png)

**Figure 3. False Error Rates**  
Shows the distribution of false errors caused by a lag in the system and the frontend.

---

## Preflight Paper Checklist

The following is the provided paper checklist. Procedures that end in A-I are separated procedures that appear in the corresponding paper quantitative evaluation.

### Required Items, Mission Equipment, and Personnel

**Personnel**:

- Crew: 3 members (Copilot, Pilot, Troop Commander)

**Weight (other)**:

- Empty: 15,000 lbs.
- 4 passengers, Cargo: 500 lbs

**A/C Configuration / Drag**:

- **Installed**: Exhaust (HIRSS), Cockpit Doors, CMWS, Med Windows, SKIS
- **Not Installed/Removed**: EIBF, Blade Erosion, All Others

### Flight Parameters

- **Presets**:  
  | Equipment/Device | Preset ID | Frequency | Band/Other |
  |------------------|-----------|-----------|-------------|
  | COM-1 | 1 | | |
  | COM-2 | 4 | | |
  | COM-3 | 5 | 127.600 | VHF-AM |
  | COM-4 | 8 | | |
  | VOR-ILS | 8 | 109.55 | |

- **Route (Figure 2)**:

  - **Departure**: Remote location: Huntsville International Airport (KHSV) (N34.159, W86.455), 889 ft
  - **Waypoints**: WAMPM -> JOSEP -> FEWER
  - **Destination**: Madison Sand Plant (MSL), 629 ft

- **Flight Parameters**:
  - Barometric Pressure: 29.92 (in. Hg)
  - Enroute Altitude: 4500 ft (between 4000 and 5000)
  - Speed/IAS (enroute): 120 kts (minimum)
  - Weather: IFR flight plan, Clear skies, no adverse weather conditions
  - Departure (MSL): 75°F / 10°C
  - Enroute (4500 ft): 57°F / 0°C
  - Destination (MSL): 80°F / 12°C

---

## Cockpit Equipment Checks

1. **Load mission data.**

   - A. CDU INI key — Press.
   - B. LSK R4 DTS CTRL soft key — Press.
   - C. Press LSK L2 — LOAD MSN DATA.
   - D. Press LSK L5 — LOAD ALL.
   - E. Press LSK L5 again (black screen) to CONFIRM.

2. **FMS Initialization**

   - A. CDU INI key — Press.
   - B. On the INITIALIZATION 1/3 page:
     - Confirm SYS time is -7 UTC as required.
     - Confirm WGS-84 is displayed.
   - C. Press NXT to page down to the INITIALIZATION 2/3 page:
     - Confirm EGI alignment is set to NAV (Navigate).
   - D. Press NXT to page down to the INITIALIZATION 3/3 page:
     - Confirm A/C GWT checks:
       - Press LSK L4 – A/C GWT.
       - Confirm empty weight as per checklist.
       - Press LSK L3 – input passengers and press ENT.
       - Press LSK R1 – input Cargo weight and press ENT.
   - E. BINGO caution checks:
     - Press CLC key.
     - Press LSK R1 – BINGO.
     - Confirm BW and BGW are equivalent and matched A/C GWT entries.

3. **Set Up MFD/COM/FMS for Mission**

   - A. FMS FPLN — Check as required.
   - B. CDU FPN key:
     - Confirm WPT SEQ — AUTO setting.
     - Press LSK L3 — FPLN LIST.
     - Press LSK L1 to IMPORT TO ALTN.
     - Press LSK R1 – REVIEW.
     - Press LSK L5 – IMPORT TO ACTV.
     - Press LSK L5 – CONFIRM.
   - C. CDU FPN key:
     - Press LSK R4 – PROCS.
     - Press LSK R2 — DEP/DEST AIRPORTS.
     - Press LSK L1 to select Destination.
     - Input destination acronym as per Checklist.
     - Press CDU ENT.
   - D. Input Frequency Preset IDs for RADIO 1 & 2 as per checklist:
     - Repeat for Radio 1 and 2:
       - Press CDU COM key.
       - Press LSK key for appropriate radio.
       - Input preset ID and Press CDU ENT.

4. **Final Check**
   - (Copilot) Confirm Pilot and Crew of GO/NGO readiness for takeoff.

---

## Adaptive Rules

The adaptive system is designed to adjust the content and modality of guidance based on pilots’ cognitive load, dynamically adapting to the demands of various flight scenarios. Below is a summary of the adaptive strategies and rules:

1. **Underload Scenarios**: Increase engagement through multimodal feedback and additional prompts.
2. **Optimal Scenarios**: Maintain steady information flow using moderate multimodal prompts.
3. **Overload Scenarios**: Reduce unnecessary information and streamline tasks.

_(Details of all 28 adaptive rules are included)_

---

## References

- Wickens, C. D. (2002). Multiple resources and performance prediction. _Theoretical Issues in Ergonomics Science_, 3(2), 159-177.
- Sweller, J. (1988). Cognitive load during problem solving: Effects on learning. _Cognitive Science_, 12(2), 257-285.
- Wickens, C. D., & Hollands, J. G. (2000). _Engineering Psychology and Human Performance_. Prentice Hall.
- Van Orden, K. F., Limbert, W., Makeig, S., & Jung, T. P. (2001). Eye activity correlates with workload during a visuospatial memory task. _Human Factors_, 43(1), 111-121.
- Spence, C., & Driver, J. (1997). Audiovisual links in endogenous covert spatial attention. _Journal of Experimental Psychology: Human Perception and Performance_, 23(5), 1333-1350.
- Parasuraman, R., & Hancock, P. A. (2008). Mitigating the adverse effects of cognitive aging on flight performance: Adaptive task allocation strategies. _The International Journal of Aviation Psychology_, 18(2), 154-183.
- Wickens, C. D., & McCarley, J. S. (2008). _Applied Attention Theory_. CRC Press.

---
