# Chip-design-vsd-Yaswanth



# Advanced Physical Design Using OpenLane and Sky130

### Inception of Open-Source EDA, OpenLane, and Sky130 PDK

#### Part 1a: RISC Instruction Set Architecture (ISA)

- **RISC-V** is a language for the computer, used in processors.
- The architecture can be implemented by **RTL (Register Transfer Level)**.

#### Circuit: Arduino Board Sample


![Screenshot (1702)](https://github.com/user-attachments/assets/07aac305-b438-47a6-8a4c-d31501a1a79c)

**Diagram of the Board:**

![Screenshot (1703)](https://github.com/user-attachments/assets/880f7d8d-ddec-4f84-9d05-999cf02ca509)


**Chip/Package:**

![Screenshot (1707)](https://github.com/user-attachments/assets/2bd296c6-4ff8-415b-8074-16dd0a771a89)


- The chip is positioned at the center or one side of the package and connected to the outer environment.

![Screenshot (1708)](https://github.com/user-attachments/assets/11378c8d-0f0d-4017-bf2a-a3f2e1a0ec6d)



- And if we open the chip we will have


![Screenshot (1710)](https://github.com/user-attachments/assets/11b9c03d-f872-431a-b05d-03962cbfeb6a)


#### RISC-V ISA Example

![Screenshot (1712)](https://github.com/user-attachments/assets/1b2935bc-2bb5-4db0-86a9-0410ef039482)

- **Foundry**: The foundry plays a crucial role in determining the chip's performance. A foundry is a factory that manufactures chips using specialized machines.
- **IP (Intellectual Property)**: Requires intelligence to design blocks within a chip.
- **Macros**: Digital logic blocks such as SPI and RISC SoC.
- **Manufacturing**: Designers need to communicate with the foundry for chip production.

![Screenshot (1713)](https://github.com/user-attachments/assets/7c6deef9-5dad-48b0-86f1-c00da42b2dd2)



### RISC-V ISA to Layout

**Steps**:

- Architecture is implemented by RTL (Register Transfer Level).

![Screenshot (1714)](https://github.com/user-attachments/assets/277615c4-1345-43d7-8a0d-5ac034e10e07)

![Screenshot (1717)](https://github.com/user-attachments/assets/fee461cb-d870-449c-bc48-247c0f52a7f4)


** Architecture of a computer **
---

![Screenshot (1731)](https://github.com/user-attachments/assets/1fd25116-4f86-4248-98e0-9e3052e64f42)


### Part 1b: RTL (Register Transfer Level)

The essential tools for creating an ASIC are **RTL IPs**, **EDA Tools**, and **PDK Data**.

![Screenshot (1734)](https://github.com/user-attachments/assets/5bc7f296-fad0-472c-bcd5-9422a93be85c)

![Screenshot (1735)](https://github.com/user-attachments/assets/20501922-5b48-4d0b-bd16-ff20c2eb3976)


#### What is a PDK?

- The **PDK** (Process Design Kit) provides the interface between the fab (foundry) and the designers.
- It includes files for:
  - **Process Design Rules (DRC, LVS, PEX)**
  - **Device Models**
  - **Digital Standard Cell Libraries**
  - **I/O Libraries**

- ANd we can also say
-   In the ‘age of Gods’ , the design of an IC was tightly integrated with the manufacturing process available within each company .

       Those who controlled physics controlled the creative agenda !

Lynn Conway and Carver Mead envisioned the the need for separating the design from technology ; 

        Pioneered the “structured” design methodology based on the  λ - based rules 


Since  then , we started to see Pure Play Fabs and Fabless design companies 

PDK  =  The interface between the FAB and the designers 
 

#### Is 130nm Process Node Outdated?

- The 130nm process may be considered old, but it is still in use in some specific applications.

![Screenshot (1738)](https://github.com/user-attachments/assets/01c14dc8-4d52-44f7-b0dc-9f2bc58a91c3)

#### Is 130nm is fast ?

![Screenshot (1739)](https://github.com/user-attachments/assets/2f04e8fb-38ff-4580-9bbe-c3b32c6f1a47)


---

### Understanding EDA Tools and the RTL to GDSII Flow

![Screenshot (1741)](https://github.com/user-attachments/assets/d92317d7-9f17-4df9-b48c-e2f6185b6773)

- Simplified RTL to GSD flow

![Screenshot (1742)](https://github.com/user-attachments/assets/ac31160b-d3e7-439c-8652-971831dddb70)


1. **Synthesis**: Convert RTL to gate-level netlist.

![Screenshot (1743)](https://github.com/user-attachments/assets/9addeadf-7a75-4275-96dc-fb4086ba108a)


![Screenshot (1745)](https://github.com/user-attachments/assets/b8e9c85d-5560-458c-89d9-a4872ff57580)


2. **Floor/Power Planning**: Plan the chip's floor layout and power distribution.

![Screenshot (1746)](https://github.com/user-attachments/assets/85d42f89-1e70-4213-85e9-28697b2f74f9)

![Screenshot (1747)](https://github.com/user-attachments/assets/34bb3ebc-62ee-4dfb-a472-1114774680b4)

![Screenshot (1748)](https://github.com/user-attachments/assets/141b314a-feb1-4787-ad2a-7c097080aa29)


3. **Placement**: Place cells on the chip's surface.

![Screenshot (1749)](https://github.com/user-attachments/assets/a6cc13b0-d194-4242-b6ee-5dfb3f2622d7)

![Screenshot (1750)](https://github.com/user-attachments/assets/4c7ccbc3-c0ef-42e9-af90-8b4595d5ca7b)


4. **Clock Tree Synthesis (CTS)**: Create the clock network.

![Screenshot (1752)](https://github.com/user-attachments/assets/5a245469-91af-4ef5-b1ba-529ea6960e85)


5. **Routing**: Route the connections between cells.

![Screenshot (1753)](https://github.com/user-attachments/assets/0404aac1-80b8-43dd-aed9-703183fc35d8)

![Screenshot (1754)](https://github.com/user-attachments/assets/79f9703d-f793-4f85-a623-b7cc5227774c)


6. **Sign-off**: Final checks to ensure the design is manufacturable.

![Screenshot (1755)](https://github.com/user-attachments/assets/49d3620a-9c9c-440a-a499-72ddb1223eb5)


#### OpenLane Overview

![Screenshot (1758)](https://github.com/user-attachments/assets/19e54537-fcf6-4194-944b-38314fda1a03)

![Screenshot (1761)](https://github.com/user-attachments/assets/c8dfd87c-a2c9-49fc-b5f2-13bfcd10f21a)


OpenLane is based on:

- **Autonomous or Interactive Operation Modes**
- **Design Space Exploration**: Find the best set of flow configurations.
- **43 Design Examples**: Best configurations for different types of designs.
- **Regression Testing**: After synthesis, use tools like Yosys for LEC (Logic Equivalence Check).


-Can be used to harden Macro chips ?

Ans :    2 modes of operation →  Autonomous   or  Interactive 

                   Design Space Exploration  :
                              Find the best set of flow configurations 

                   Large no.of design examples 
                              43 designs with their best configurations 
                              More will be added soon 

---

### Physical Design Flow

![Screenshot (1771)](https://github.com/user-attachments/assets/05c0a72b-c22e-4997-a773-6c59c0a2372c)

![Screenshot (1772)](https://github.com/user-attachments/assets/e67114d9-f868-46f5-aa28-1af6fe195620)

![Screenshot (1773)](https://github.com/user-attachments/assets/cc4715f9-6ad8-4d81-a775-eda0d8d27c61)

![Screenshot (1774)](https://github.com/user-attachments/assets/15b5f9ab-3cc5-4989-acae-feb004624580)

![Screenshot (1775)](https://github.com/user-attachments/assets/f4844daa-f8d8-40ee-99d5-09c0304b0f09)


After **synthesis**, we follow steps like:

1. **DFT (Design for Test)**: Add fault-tolerant features to the chip.

![Screenshot (1777)](https://github.com/user-attachments/assets/cc3caa72-c83c-4a8e-a1cd-010ba4cbd56f)

2. **Physical Implementation**: Begin the physical design process.

![Screenshot (1778)](https://github.com/user-attachments/assets/84e044f7-1f79-4a95-99e7-02a83edae580)

3. **LEC**: Ensure logic equivalence between RTL and the gate-level design.

![Screenshot (1779)](https://github.com/user-attachments/assets/1ae5e3d2-bd0c-40fb-8913-ee1341b1d846)

4. **Fake ant , diodes and Insertion Script / Dealing with Antenna Rules Violation**

![Screenshot (1781)](https://github.com/user-attachments/assets/6d029065-6ef6-4fca-86eb-9b3c39ff420b)




5. **RC Extraction** → **STA (Static Timing Analysis)** → **Physical Verification**.



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
