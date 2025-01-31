# Chip-design-vsd-Yaswanth



# Advanced Physical Design Using OpenLane and Sky130

### Inception of Open-Source EDA, OpenLane, and Sky130 PDK

#### Part 1a: RISC Instruction Set Architecture (ISA)

- **RISC-V** is a language for the computer, used in processors.
- The architecture can be implemented by **RTL (Register Transfer Level)**.

#### Circuit: Arduino Board Sample

**Diagram of the Board:**

![Yaswanth](Screenhot(1702))

**Chip/Package:**



- The chip is positioned at the center or one side of the package and connected to the outer environment.

#### RISC-V ISA Example

- **Foundry**: The foundry plays a crucial role in determining the chip's performance. A foundry is a factory that manufactures chips using specialized machines.
- **IP (Intellectual Property)**: Requires intelligence to design blocks within a chip.
- **Macros**: Digital logic blocks such as SPI and RISC SoC.
- **Manufacturing**: Designers need to communicate with the foundry for chip production.

### RISC-V ISA to Layout

**Steps**:

- Architecture is implemented by RTL (Register Transfer Level).

---

### Part 1b: RTL (Register Transfer Level)

The essential tools for creating an ASIC are **RTL IPs**, **EDA Tools**, and **PDK Data**.

#### What is a PDK?

- The **PDK** (Process Design Kit) provides the interface between the fab (foundry) and the designers.
- It includes files for:
  - **Process Design Rules (DRC, LVS, PEX)**
  - **Device Models**
  - **Digital Standard Cell Libraries**
  - **I/O Libraries**

#### Is 130nm Process Node Outdated?

- The 130nm process may be considered old, but it is still in use in some specific applications.

---

### Understanding EDA Tools and the RTL to GDSII Flow

1. **Synthesis**: Convert RTL to gate-level netlist.
2. **Floor/Power Planning**: Plan the chip's floor layout and power distribution.
3. **Placement**: Place cells on the chip's surface.
4. **Clock Tree Synthesis (CTS)**: Create the clock network.
5. **Routing**: Route the connections between cells.
6. **Sign-off**: Final checks to ensure the design is manufacturable.

#### OpenLane Overview

OpenLane is based on:

- **Autonomous or Interactive Operation Modes**
- **Design Space Exploration**: Find the best set of flow configurations.
- **43 Design Examples**: Best configurations for different types of designs.
- **Regression Testing**: After synthesis, use tools like Yosys for LEC (Logic Equivalence Check).

---

### Physical Design Flow

After **synthesis**, we follow steps like:

1. **DFT (Design for Test)**: Add fault-tolerant features to the chip.
2. **Physical Implementation**: Begin the physical design process.
3. **LEC**: Ensure logic equivalence between RTL and the gate-level design.
4. **RC Extraction** → **STA (Static Timing Analysis)** → **Physical Verification**.

#### Define Width and Height of Core and Die

- **Core**: The central region that holds the logic cells.
- **Die**: The overall chip's physical area.

#### Example: Placement of Cells

- Pre-placed cells should be surrounded by decoupling capacitors.
- The core of the chip should contain all logical cells.

#### Power Planning and Pin Placement

- Ensure proper **pin placement** for efficient power distribution.

---

### Timing and Signal Integrity

- **Timing Characterization**: Check **propagation delay** and **transition time**.
- **Spice Decks**: Use spice simulations to measure delays and waveforms for rise and fall times.
  
---

### Fabrication Process: 16nm CMOS

- In some cases, the **photolithography** process involves UV light, Boron, Arsenic, and other materials.

---

### Power-Aware Clock Tree Synthesis (CTS)

- Focus on **timing analysis**:
  - **Setup Timing Analysis**
  - **Hold Timing Analysis**
  
### Routing and Optimization

- Ensure the grid boxes are numbered and the signal integrity is maintained.

#### Final Steps:

- **Buffering**: Use repeaters (buffers) to maintain signal quality over distance.
