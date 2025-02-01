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



![Screenshot (1752)](https://github.com/user-attachments/assets/45cc936a-bd1f-41b8-b244-39fc8c300a33)


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

![Screenshot (1781)](https://github.com/user-attachments/assets/c76e50fa-3eb2-4f1c-bb21-9e00dc57de44)

![Screenshot (1783)](https://github.com/user-attachments/assets/8228a72b-aa60-44a7-afe9-8492e8ae1716)

![Screenshot (1784)](https://github.com/user-attachments/assets/ac0e4181-176d-401b-bfba-8b4fdcba8cc3)



5. **RC Extraction** → **STA (Static Timing Analysis)** → **Physical Verification**.

![Screenshot (1785)](https://github.com/user-attachments/assets/28042fba-da7f-4b50-bbf6-4d603a45270e)

![Screenshot (1787)](https://github.com/user-attachments/assets/8d2b1aa1-e9e8-46bf-bab0-61eebd8f1200)



#### Define Width and Height of Core and Die

![Screenshot (1788)](https://github.com/user-attachments/assets/c91957c7-efc1-4e7f-8642-9344964574c4)

![Screenshot (1789)](https://github.com/user-attachments/assets/5e23dc44-ee0d-4eb2-999b-73988e071ec5)

![Screenshot (1790)](https://github.com/user-attachments/assets/6c054ca2-e2ec-4a62-b15c-d419f93e5da0)

![Screenshot (1791)](https://github.com/user-attachments/assets/0bab6e5a-3242-4c58-8070-a0decc85dd5f)


- **Core**: The central region that holds the logic cells

![Screenshot (1792)](https://github.com/user-attachments/assets/50e16f8f-0094-44eb-8bd1-c7b8441f998a)


- **Die**: The overall chip's physical area.

![Screenshot (1793)](https://github.com/user-attachments/assets/3fba0cc2-f10b-440a-938c-2e7634563c1b)

#### Dimensions

![Screenshot (1794)](https://github.com/user-attachments/assets/bbc306bf-9bcf-4031-a85e-7f5dd5aac829)

![Screenshot (1797)](https://github.com/user-attachments/assets/757d7ca1-68e4-4d72-9c4f-2fb393a4bab8)

![Screenshot (1798)](https://github.com/user-attachments/assets/25fa4588-3df4-4e8a-a755-f78b13c3a7f9)

![Screenshot (1799)](https://github.com/user-attachments/assets/1c882f37-a76f-4274-97a3-f8ae3272c9cc)

![Screenshot (1802)](https://github.com/user-attachments/assets/4617dd17-c616-40e0-9756-68c4476ff62a)

![Screenshot (1803)](https://github.com/user-attachments/assets/0058a545-c2bc-4fb9-8522-d8f49dc98e4b)

![Screenshot (1806)](https://github.com/user-attachments/assets/945cfcf1-13b6-49d5-852c-aa6ac0cc70db)

![Screenshot (1807)](https://github.com/user-attachments/assets/551b7b3f-cc7e-4c6c-97d2-5433f430b667)

![Screenshot (1808)](https://github.com/user-attachments/assets/496e2f71-f9dc-4c48-90b3-ad24cf7629ae)

![Screenshot (1809)](https://github.com/user-attachments/assets/041ef5ac-2d2f-43e5-8696-96b759cfcb1e)

![Screenshot (1810)](https://github.com/user-attachments/assets/6490fd0d-37b6-498d-b94d-05380778321d)


#### Placement of Cells


![Screenshot (1823)](https://github.com/user-attachments/assets/90f0fe1d-b563-4554-8c25-58e3cf37fda6)

![Screenshot (1824)](https://github.com/user-attachments/assets/a8dfc17a-bff6-4a83-a634-1acc52966ffe)

![Screenshot (1825)](https://github.com/user-attachments/assets/d5d71e81-eba2-4c38-8780-8dedf87c28ee)

![Screenshot (1826)](https://github.com/user-attachments/assets/b6867868-e3bd-42e3-8de8-27c330277a14)

![Screenshot (1827)](https://github.com/user-attachments/assets/8d68405c-180f-46dc-9592-b2d9b88c4e16)


- Pre-placed cells should be surrounded by decoupling capacitors.
- The core of the chip should contain all logical cells.


#### Surround the pre placed cellswith decoupling capacitors


![Screenshot (1828)](https://github.com/user-attachments/assets/7b06a313-6aa6-45db-9bf0-c41220479e12)

![Screenshot (1829)](https://github.com/user-attachments/assets/a3ac3442-6c9e-405b-a72c-a495823a01c7)

![Screenshot (1830)](https://github.com/user-attachments/assets/0dcc7251-365b-4a75-b25a-f8ac13d13c7f)

![Screenshot (1831)](https://github.com/user-attachments/assets/e2a07be9-b65b-4054-a346-2656220a6a59)

![Screenshot (1832)](https://github.com/user-attachments/assets/d6ccce67-6f98-42eb-8895-f6a3f842469b)

![Screenshot (1833)](https://github.com/user-attachments/assets/4ff3aa23-4cbd-47c8-ba80-123c3abad2fd)

![Screenshot (1834)](https://github.com/user-attachments/assets/16b73334-2876-4294-9533-bab9f174a1a9)

![Screenshot (1835)](https://github.com/user-attachments/assets/e2eae6ee-2776-4e05-b4dc-bb31c56cd805)




#### Power Planning and Pin Placement

![Screenshot (1836)](https://github.com/user-attachments/assets/9911e24c-92fd-4159-89fc-adf992d057d7)

![Screenshot (1837)](https://github.com/user-attachments/assets/c2eb9a2c-26bf-46a6-bef5-84baffd6e0a1)

![Screenshot (1838)](https://github.com/user-attachments/assets/1c166bf1-cfb5-4f81-a75d-ab98d1394205)

![Screenshot (1839)](https://github.com/user-attachments/assets/1dc25ba6-2386-4b58-84ee-83774aa05bdf)

![Screenshot (1840)](https://github.com/user-attachments/assets/39a0035c-f33e-427b-be86-829092e8bbc7)

![Screenshot (1841)](https://github.com/user-attachments/assets/4b5581d1-793c-4f1c-a761-96b280587143)

![Screenshot (1842)](https://github.com/user-attachments/assets/020410e7-f7db-4352-aee4-0f9ac2682575)

![Screenshot (1843)](https://github.com/user-attachments/assets/c1d3c4cb-c961-4672-a168-af006a71caf7)

![Screenshot (1844)](https://github.com/user-attachments/assets/205e8da9-9435-4c8f-aee5-180bd6fac499)

![Screenshot (1845)](https://github.com/user-attachments/assets/e7edbdd1-42b8-417c-b865-0e62535fb52a)

![Screenshot (1846)](https://github.com/user-attachments/assets/ebdb1439-2538-44dd-985e-9c7fff0c3af2)

![Screenshot (1846)](https://github.com/user-attachments/assets/00d7dd32-5609-44b3-ba90-12a1228e53c5)

![Screenshot (1847)](https://github.com/user-attachments/assets/5a4ac801-1ca3-4ab6-bef0-47ac22fd8c5d)

![Screenshot (1848)](https://github.com/user-attachments/assets/3e47a777-fff2-4d07-bf5d-b3edb9d89022)

![Screenshot (1849)](https://github.com/user-attachments/assets/4364764c-5ac2-4fe3-8593-3230f9ba4ee6)

![Screenshot (1850)](https://github.com/user-attachments/assets/94d667e8-6585-4a28-ae16-202bcaac48ac)

![Screenshot (1851)](https://github.com/user-attachments/assets/522437a1-49d0-4687-8b70-5867990ee6d2)

### Logical cell placement blockage

    #### 1) Bind netlist with physical cells


![Screenshot (1851)](https://github.com/user-attachments/assets/7c28bf3f-7510-4c65-b217-39c4129afc19)


![Screenshot (1852)](https://github.com/user-attachments/assets/5f551b45-b91b-4935-ac36-46461d907eb1)


![Screenshot (1853)](https://github.com/user-attachments/assets/2a05409a-716f-4ca1-9d6b-09d09ffd8a09)


![Screenshot (1854)](https://github.com/user-attachments/assets/21eb32e5-8e7f-40e8-b23c-1c0e3a844e6e)


![Screenshot (1855)](https://github.com/user-attachments/assets/a486a228-9e92-420d-890a-230cf5bf489e)


![Screenshot (1856)](https://github.com/user-attachments/assets/49c260c4-537a-4e65-a059-0edd88833695)


![Screenshot (1857)](https://github.com/user-attachments/assets/8f8dd328-5965-41af-8806-79767952c833)


![Screenshot (1858)](https://github.com/user-attachments/assets/2ae88d32-33ac-468c-95f7-bc1c7a1f21fe)



  #### 2) Placement



![Screenshot (1859)](https://github.com/user-attachments/assets/d3649042-542a-43c3-9282-b011e7987aba)


![Screenshot (1860)](https://github.com/user-attachments/assets/56156810-83d1-4f9d-a90e-8cb84ac1bdce)


- to solve the problem we optimize placement :

   #### 3) OPtiize placement
    
- this topic is based o the signal integrity

![Screenshot (1874)](https://github.com/user-attachments/assets/0e90e445-3faf-4f37-9203-8b0b36404842)


![Screenshot (1875)](https://github.com/user-attachments/assets/6d337e6a-b8c3-4c33-9c78-751e55637ea7)

![Screenshot (1876)](https://github.com/user-attachments/assets/b1612172-0100-4242-8d64-8b717401511a)

![Screenshot (1877)](https://github.com/user-attachments/assets/895dc162-e234-4924-b818-23046f83dbe6)

![Screenshot (1879)](https://github.com/user-attachments/assets/53caff80-fe8d-4259-b6b1-038f5daaa4e5)

![Screenshot (1881)](https://github.com/user-attachments/assets/655f44d7-4267-414c-a8be-0945e8b5d1a2)

![Screenshot (1882)](https://github.com/user-attachments/assets/a526057e-4c42-4d16-a214-913520035aa9)

![Screenshot (1883)](https://github.com/user-attachments/assets/58e18204-b7e1-4e68-a2d6-a6314e76670e)

![Screenshot (1884)](https://github.com/user-attachments/assets/b3aac2cf-5fa1-4f91-be61-3c1d2d0573f6)

![Screenshot (1885)](https://github.com/user-attachments/assets/bd0c238c-4bbf-4398-b315-42bcd7a45372)

![Screenshot (1886)](https://github.com/user-attachments/assets/7dd61650-61b3-457d-adbf-6883f70617f0)

![Screenshot (1887)](https://github.com/user-attachments/assets/50939535-d204-4040-a14c-7d59d2d4707a)

![Screenshot (1890)](https://github.com/user-attachments/assets/f3bacfff-fc25-4c8b-96a2-63255a5b9a61)

![Screenshot (1888)](https://github.com/user-attachments/assets/72765e33-c6db-4d01-9976-6d3d06acc65f)



- **Buffering**: Use repeaters (buffers) to maintain signal quality over distance
- - Ensure proper **pin placement** for efficient power distribution.

---

### Cell design flow

![Screenshot (1894)](https://github.com/user-attachments/assets/4280f033-0bff-4fc3-8442-06bf8b86ad4b)
![Screenshot (1895)](https://github.com/user-attachments/assets/be226c5f-eaa7-45b7-82f1-d16d4bf2db5f)

![Screenshot (1896)](https://github.com/user-attachments/assets/bebfe825-1458-4598-a0d2-a3d7921af610)

![Screenshot (1897)](https://github.com/user-attachments/assets/084b0b9f-5719-49fd-8f88-78170161d75d)

![Screenshot (1898)](https://github.com/user-attachments/assets/3ae87524-42ac-4c49-a050-694faead8209)

![Screenshot (1899)](https://github.com/user-attachments/assets/da16c189-56c1-4a77-a178-e9cf4b566643)

![Screenshot (1900)](https://github.com/user-attachments/assets/e50b1b4d-4a44-45c3-81d4-c7694e30e6c6)

![Screenshot (1901)](https://github.com/user-attachments/assets/c6fd8981-aed6-4114-8e10-e7e393ad3f97)

![Screenshot (1902)](https://github.com/user-attachments/assets/bfb24dd1-41b7-425b-87d5-94e2042db1a3)

![Screenshot (1903)](https://github.com/user-attachments/assets/3a05418f-f520-4a56-accb-3f0e7f18e719)

![Screenshot (1904)](https://github.com/user-attachments/assets/bef40543-56cf-4a5a-81f7-9a796f418aa2)

![Screenshot (1905)](https://github.com/user-attachments/assets/e6fe3f20-7b0b-4c7f-adfb-51f8fbecff88)

![Screenshot (1906)](https://github.com/user-attachments/assets/b9fa9202-5ceb-452e-92f9-cbced1e9cfb0)

![Screenshot (1907)](https://github.com/user-attachments/assets/b475d722-43da-4308-8ec3-5f6f583966d4)

![Screenshot (1908)](https://github.com/user-attachments/assets/341c51e9-da47-4038-a45f-eaacae3bdc08)

![Screenshot (1909)](https://github.com/user-attachments/assets/28f0372c-3300-458c-ad77-c6bfbb7df71c)

![Screenshot (1910)](https://github.com/user-attachments/assets/afa27f01-a0c2-444b-8c0c-e958e92d99ea)

![Screenshot (1911)](https://github.com/user-attachments/assets/37ae19dc-37dc-42ed-98c7-37f5da7ebddd)

![Screenshot (1912)](https://github.com/user-attachments/assets/3019dcec-3a3b-4dce-be79-d01b2d34ab3a)

![Screenshot (1913)](https://github.com/user-attachments/assets/10b5a576-7c16-4a6c-8298-20f154183e9f)

![Screenshot (1914)](https://github.com/user-attachments/assets/1df072fd-6d1c-42cc-9813-d33ed9dcaaaa)


  #### Characterization flow


![Screenshot (1915)](https://github.com/user-attachments/assets/800d8164-b0e5-48de-af55-cb1202723dd3)

![Screenshot (1920)](https://github.com/user-attachments/assets/b5118501-d214-42b5-a535-11cb344e5817)

![Screenshot (1922)](https://github.com/user-attachments/assets/96bfcdc2-fd9f-4dc5-943b-bdf59c41f862)

![Screenshot (1923)](https://github.com/user-attachments/assets/f83cb9c9-7732-41a7-a512-fe71aad75647)

![Screenshot (1921)](https://github.com/user-attachments/assets/ec81a594-527b-4487-b7ca-8a151e78dbd2)

![Screenshot (1922)](https://github.com/user-attachments/assets/489aa2ea-ae85-4f66-92df-1fb64b840ceb)

![Screenshot (1923)](https://github.com/user-attachments/assets/73ab66f4-3b90-40c1-ad61-27fe1dc85be7)

![Screenshot (1924)](https://github.com/user-attachments/assets/0daaf4e1-6b1a-4159-80ac-0f55be590ceb)

![Screenshot (1925)](https://github.com/user-attachments/assets/2cbabe8a-e352-4fa9-9400-6dbe470a674d)

![Screenshot (1926)](https://github.com/user-attachments/assets/71e9eeff-fc0f-494b-80c8-ae114f543783)

![Screenshot (1927)](https://github.com/user-attachments/assets/540ed014-8bc0-4be1-a961-527400a98f47)

![Screenshot (1928)](https://github.com/user-attachments/assets/17dc5f5a-069c-43e8-a2b7-103c2b28a550)

![Screenshot (1929)](https://github.com/user-attachments/assets/0b5493ce-65e3-41d1-8d23-a734f81fa138)



### Timing and Signal Integrity

- **Timing Characterization**: Check **propagation delay** and **transition time**.


![Screenshot (1930)](https://github.com/user-attachments/assets/46754133-6867-4841-a25e-fc081d50fe1a)

![Screenshot (1931)](https://github.com/user-attachments/assets/ed645609-63b8-4e27-91e0-b68ebdd09847)

![Screenshot (1932)](https://github.com/user-attachments/assets/949ec5ac-7735-4fd5-af7e-6fb49129311c)

![Screenshot (1933)](https://github.com/user-attachments/assets/d538d7b5-85b7-474b-9bf3-5ace535b34b4)

![Screenshot (1934)](https://github.com/user-attachments/assets/611c3cf7-ccd6-4bbb-a24f-f1db14c9f013)

![Screenshot (1935)](https://github.com/user-attachments/assets/7bd1de80-2c38-44e7-85fe-197dbddd0bf4)

![Screenshot (1936)](https://github.com/user-attachments/assets/24f93497-7fc0-448e-b343-ccc3fa1fb469)

![Screenshot (1937)](https://github.com/user-attachments/assets/b95add0b-ec04-468a-8929-136bcc6f9531)

![Screenshot (1938)](https://github.com/user-attachments/assets/ff7679ba-170b-4c08-b2e0-5f259f2ac40a)

![Screenshot (1939)](https://github.com/user-attachments/assets/9c5f5c03-416a-4739-8036-47074d85b9bb)

![Screenshot (1940)](https://github.com/user-attachments/assets/c4e53678-07cf-440e-a706-e47d55ce965b)

![Screenshot (1941)](https://github.com/user-attachments/assets/fc79e3bb-708d-4d8c-aebb-439c2cbf0270)

![Screenshot (1942)](https://github.com/user-attachments/assets/9a087168-e690-449f-879b-b360d2ccb487)

![Screenshot (1943)](https://github.com/user-attachments/assets/84372fce-98fa-4807-b769-d2ba6bf24ace)

![Screenshot (1944)](https://github.com/user-attachments/assets/ca55d033-ff96-4dcb-8ae7-915917674411)

![Screenshot (1945)](https://github.com/user-attachments/assets/635a1fba-7bbc-4475-9841-7ab83f590755)






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



