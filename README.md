# ev-driveline-charging
Simulink-based DC charging controller for EVs with multiple drivelines.

# EV Driveline Charging Controller

This project demonstrates a **Simulink-based charging control system** for electric vehicles (EVs) equipped with **multiple drivelines and battery packs**. The system ensures intelligent battery selection and safe charging strategy in DC charging scenarios.

## Project Scope

In most EVs, only one battery pack is charged at a time using standard DC charging protocols. This project addresses the challenge of **sequentially charging multiple driveline batteries** in a way that:
- Balances state-of-charge (SoC) across all battery packs.
- Minimizes thermal stress by not focusing on a single battery.
- Selects which driveline to charge based on SoC comparison.

## Control Strategy

- A custom **MATLAB Function Block** identifies the battery with the lowest SoC.
- A selection algorithm decides when to switch to the next battery.
- The controller ensures that each battery is charged until it reaches at least 2% above the next-lowest SoC.
- Charging stops when all batteries are fully charged.

## Model Highlights

- Simulink model includes:
  - Mathematical battery models (3 total)
  - Charging controller subsystem
  - Selection logic and state machines
- Outputs include SoC tracking and battery state logic for each driveline.

## Results (Plots)

Charging behavior is visualized through SoC graphs that reflect the intelligent, non-simultaneous charging process. Each battery’s SoC rises in coordination to prevent overcharging or imbalance.

## Project Documentation

You can view the full project report with Simulink diagrams and detailed explanations in this PDF:

 
 [Download Project Report (PDF)](https://github.com/GuzinGunduz/ev-driveline-charging/blob/main/SelectDrivelineGuzin%20(1).pdf)


## Tools Used

- MATLAB / Simulink
- Model-Based Design principles

---

> Author: **Guzin Gunduz**  

