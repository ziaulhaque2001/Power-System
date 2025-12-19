# Power-System
System analysis using python code


Problem 1-

This is a university assignment document about analyzing an electrical power system. The project involves studying a small model power grid with 6 connection points (called "buses") and performing two types of technical analyses on it. The student must write a computer program, produce results, and then explain their work in a report and oral examination.
Core Task
The main assignment has three computational parts and one comparative part:
1. First Analysis (Normal Conditions): Perform a "load-flow analysis." This means calculating how power normally flows through the system when it is supplying electricity to customers. You need to find the voltage at each bus, calculate the total power lost as heat in the wires, and create a diagram showing the power flow on each line.
2. Second Analysis (Fault Conditions): Perform a "symmetrical three-phase short circuit analysis" for a specific severe fault (like a bolt dropping and connecting all three phases directly together) at Bus 6. For this scenario, you must calculate:
   * The massive fault current that would flow.
   * What the voltage would be at every bus during the fault.
   * What the current would be in every power line during the fault.
   * The "Short-Circuit Capacity" (SCC), which is a measure of the system's strength at that point.
3. Third Task (More Faults): Repeat the detailed short-circuit analysis from Part 2 for the same type of severe fault, but this time at Bus 4 and then at Bus 5.
4. Fourth Task (Comparison): Compare the calculated Short-Circuit Capacity (SCC) values for fault locations at Buses 4, 5, and 6. This shows which bus is connected to the strongest part of the grid (highest SCC) and which is the weakest (lowest SCC).
Report and Assessment Requirements
* Formal Report: The student must submit a report containing the input data file they created, a list of the computer programs they selected or wrote, and all results presented in organized tables.
* Oral Examination ("Viva"): The student must thoroughly understand the programs and results, as they will face a comprehensive oral test on the project. The quality of both the report and the oral performance are important for the final grade.
* Demonstration: The student must bring a laptop with the programs to demonstrate their work.
System Data Tables
The document provides four tables with all the necessary numbers to model the system. All values are in a normalized format called "per unit (pu)" on a base of 100 Mega-Volt-Amperes (MVA).
Table 1: Line and Transformer Data
This table describes the electrical properties of the wires and transformers that connect the buses. Each row is a connection between two buses. The columns are:
* Bus No.: The starting bus number.
* Bus No.: The ending bus number.
* R (PU): The resistance of the connection, which causes real power loss as heat.
* X (PU): The reactance of the connection, which affects voltage levels and limits power flow.
* ½ B (PU): Half of the total capacitive charging susceptance of the line.
The specific connections and their values are:
* A line connects Bus 1 to Bus 4 with R=0.035, X=0.225, ½B=0.0065.
* A line connects Bus 1 to Bus 5 with R=0.025, X=0.105, ½B=0.0045.
* A line connects Bus 1 to Bus 6 with R=0.040, X=0.215, ½B=0.0055.
* A transformer connects Bus 2 to Bus 4 with R=0.000, X=0.035, ½B=0.0000.
* A transformer connects Bus 3 to Bus 5 with R=0.000, X=0.042, ½B=0.0000.
* A line connects Bus 4 to Bus 6 with R=0.028, X=0.125, ½B=0.0035.
* A line connects Bus 5 to Bus 6 with R=0.026, X=0.175, ½B=0.0300.
Table 2: Generator Transient Impedance
This table provides a key parameter for each of the three generators needed only for the short-circuit analysis. The columns are:
* Gen. No.: The generator number (1, 2, or 3).
* Rₐ: The armature resistance (all are 0 in this case).
* X'ₐ: The "transient reactance," a value critical for calculating high fault currents.
   * Generator 1: X'ₐ = 0.20 pu
   * Generator 2: X'ₐ = 0.15 pu
   * Generator 3: X'ₐ = 0.25 pu
Table 3: Generation Schedule
This table defines the operating conditions for the three generator buses. The columns are:
* Bus No.: The bus where the generator is located (1, 2, 3).
* Voltage Mag.: The target voltage magnitude the generator must maintain.
* Generation (MW): The scheduled real power output from the generator in Megawatts.
* Mvar Limits (Min. / Max.): The minimum and maximum reactive power output limits for the generator in Mega-volt-amperes-reactive.
The specific generator data is:
* Bus 1: Voltage = 1.06 pu. It is the "slack" or "swing" bus, meaning its real and reactive power output are not scheduled but adjust to balance the entire system. No generation MW or limits are listed for it.
* Bus 2: Voltage = 1.04 pu, Generation = 150 MW, Reactive limits between 0 and 140 Mvar.
* Bus 3: Voltage = 1.03 pu, Generation = 100 MW, Reactive limits between 0 and 90 Mvar.
Table 4: Load Data
This table lists the electrical demand from customers at each bus. The columns are:
* Bus No.: The bus number (1 through 6).
* Load MW: The real power consumption in Megawatts.
* Load Mvar: The reactive power consumption in Mega-volt-amperes-reactive.
The specific load data is:
* Buses 1, 2, and 3: 0 MW, 0 Mvar (These are pure generation buses).
* Bus 4: 100 MW, 70 Mvar.
* Bus 5: 90 MW, 30 Mvar.
* Bus 6: 160 MW, 110 Mvar.
Hint for Students
A note from the instructor suggests:
1. Use a power flow program to get the normal "pre-fault" bus voltages and to model the load as an admittance.
2. Study textbook examples and choose the right programs.
in case u cant see the document properly here is a text form
