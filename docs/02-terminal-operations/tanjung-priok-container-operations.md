# **End-to-End Operational Architecture and Transit Flow Analysis of Containerized Cargo at the Port of Tanjung Priok**

## **1\. End-to-End Operational Lifecycle: Marine, Quayside, Yard, Customs, and Landside Multimodal Flows**

The Port of Tanjung Priok (UN/LOCODE: IDTPP) operates as Indonesia’s preeminent international trade gateway, consolidating more than 50% of the archipelago's containerized cargo volume and generating an annual throughput surpassing 8 million Twenty-Foot Equivalent Units (TEUs)1. Terminal infrastructure is partitioned among primary commercial terminal operating entities: the Jakarta International Container Terminal (JICT), Terminal Petikemas Koja (TPK Koja), New Priok Container Terminal 1 (NPCT1 / Kalibaru), and IPC Terminal Petikemas (IPC TPK Area 1, 2, and 3\)1. The operational lifecycle of import and export container handling spans seven strictly sequenced functional phases governed by marine navigation protocols, heavy handling machinery, digital platform integrations, and multi-agency regulatory checkpoints.

### **Phase 1: Pre-Arrival Manifesting, Stowage Planning, and Berth Allocation**

The maritime transit cycle initiates 24 to 72 hours prior to vessel arrival at Tanjung Priok outer anchorage1. Shipping lines and handling agents submit the vessel arrival notification (Pemberitahuan Kedatangan Kapal \- PKK) alongside pilotage and towage requisitions (Permohonan Pelayanan Kapal \- PPK) directly into Inaportnet, the Ministry of Transportation’s digital maritime portal1. In parallel, shipping line planners transmit electronic manifests and bay plans to the receiving terminal’s Terminal Operating System (TOS) via Electronic Data Interchange (EDI) standards, primarily BAPLIE (Bayplan In Transit Delays / Empty Containers) message files7.  
Terminal berth and vessel planners ingest this telemetry to formulate operational discharge and loading sequences. Planners analyze vessel physical constraints—including draft relative to tidal curves, overall length (LOA), beam, displacement, and onboard crane configurations—against quayside assets8. The TOS determines precise quay crane assignments and crane split distributions, while vessel planners construct the crane working schedule to balance quay cycle times with yard receiving capacities. Concurrently, yard planners designate initial stacking blocks in the container yard (CY), segregating import discharge assignments from export stacks and hazardous materials to prevent equipment contention.

### **Phase 2: Harbor Approach, Vessel Traffic Management, Pilotage, and Berthing**

Vessels arriving at the outer roads enter the territorial jurisdiction of the Kantor Otoritas Pelabuhan Utama Tanjung Priok and the Harbour Master (Kantor Kesyahbandaran dan Otoritas Pelabuhan \- KSOP)1. Approach monitoring is maintained through the port's Vessel Traffic Management System (VTMS)7. Under Indonesian maritime law, pilotage is strictly compulsory for commercial container vessels within the navigation fairway1. Pelindo Marine Services dispatches licensed harbor pilots via pilot boats operating continuously around the clock to meet vessels at designated outer boarding grounds1.  
Upon boarding and the completion of the master-pilot information exchange, the pilot navigates the vessel through the breakwater into the main fairway, which spans 150 meters in width and is dredged to a nominal depth of \-14 meters Mean Lower Low Water (MLLW)1. Pelindo tugboats—typically deploying two to four azimuth stern drive tugs rated between 3,200 and 5,000 brake horsepower (BHP)—assist in speed deceleration and precision turning maneuvers within the inner basin. Quayside berthing maneuvers adhere to strict hydrodynamic tolerances: vessel approach velocity is governed to stay below 0.10 to 0.15 meters per second at an angle of approach under 10 degrees to protect the cell-type rubber marine fender systems8. Terminal line-handling gangs secure the vessel onto quay bollards engineered to withstand tractive mooring forces between 100 and 150 metric tons8. Once moored, port health authorities grant quarantine free pratique, the Harbour Master issues inward port clearance, and stevedoring gangs (Tenaga Kerja Bongkar Muat \- TKBM) rig vessel access gangways1.

### **Phase 3: Quayside Discharging and Horizontal Quay-to-Yard Drayage**

Quayside stevedoring is executed using rail-mounted Ship-to-Shore (STS) Super Post-Panamax or Post-Panamax container gantry cranes10. Operations commence when the TOS transmits discharge sequences wirelessly to the onboard crane management system and terminal prime movers. Crane operators position spreaders equipped with semi-automatic or fully automated twistlock engagement frames directly over vessel deck cells or open cargo holds. The spreader locks onto the container corner castings, lifts the unit out of the cell guides, and transfers it horizontally across the quay apron10.  
On the apron, stevedoring unlashing personnel remove semi-automatic twistlocks (SATLs). The container is lowered directly onto an awaiting internal terminal tractor-trailer unit (Terminal Truck / Internal Prime Mover)10. Tally personnel or automated optical character recognition (OCR) systems mounted on the crane portal structure capture the container ISO code, chassis identifier, and seal condition, transmitting completion timestamps to the TOS core7. The internal hauler then transports the container along designated internal terminal traffic corridors to the designated yard stack10.

### **Phase 4: Container Yard Marshaling, RTG Operations, and Dwell-Time Governance**

Upon reaching the assigned storage block, yard cranes—principally Rubber-Tired Gantry (RTG) cranes, Electric RTGs (e-RTGs), or Automated Stacking Cranes (ASCs)—lift the container from the internal truck chassis10. The TOS instructs the yard crane operator to lower the container into a specific ground slot identified by bay, row, and tier coordinates10. Yard equipment utilizes Differential GPS (DGPS) and Position Detection Systems (PDS) to automatically confirm that the physical placement matches the assigned digital address.  
Stack configuration follows strict operational heuristics designed to minimize non-productive rehandling while respecting structural load limits:

* Hazardous cargo (IMO classes) is directed toward dedicated containment compounds equipped with specialized drainage and fire suppression infrastructure.  
* Temperature-controlled containers (reefers) are drayed immediately to reefer gantries and plugged into monitoring stations, where technicians verify setpoints and electrical telemetry11.  
* General import containers are stacked four to five containers high, organized by discharge rotation, consignee customs clearance profiling, and anticipated clearance pathways to minimize reshuffling upon retrieval10.

Terminal managers monitor the Yard Occupancy Rate (YOR), maintaining yard density below 70% of gross holding capacity to preserve fluidity and prevent equipment congestion10.

### **Phase 5: Customs Clearance, Quarantine Integration, and Physical Inspection**

The regulatory lifecycle operates through parallel digital networks connecting the Directorate General of Customs and Excise (Direktorat Jenderal Bea dan Cukai \- DJBC via KPU Bea dan Cukai Tipe A Tanjung Priok), the Indonesia National Single Window (LNSW), and the National Logistics Ecosystem (NLE)1. The customs broker (PPJK) or importer lodges the Import Declaration (Pemberitahuan Impor Barang \- PIB) into the CEISA 4.0 customs mainframe7. CEISA evaluates the declaration through automated risk algorithms, cross-referencing cargo manifests and merchant compliance histories to categorize the shipment into one of three administrative processing tracks10:

* **Green Channel**: Import declarations require no documentary audit or physical examination. Customs duties, value-added taxes (PPN), and income taxes (PPh 22\) are settled via electronic treasury accounts, prompting CEISA to automatically issue an electronic Customs Release Approval (Surat Persetujuan Pengeluaran Barang \- SPPB)10.  
* **Yellow Channel**: Declarations undergo documentary auditing. Customs verification officers review digital trade documentation, including commercial invoices, packing lists, and preferential certificates of origin, within the CEISA interface. Once cleared, the SPPB is transmitted electronically without cargo intervention.  
* **Red Channel**: Requires both full documentary audit and mandatory physical inspection (Behandle)10. CEISA issues a Red Channel Notification (Surat Pemberitahuan Jalur Merah \- SPJM) to both the importer and the terminal17.

For cargo requiring biological, phytosanitary, or agricultural oversight, the Single Submission Quarantine Customs (SSm QC) platform synchronizes the inspection process15. This unified interface connects customs examiners and Indonesian Quarantine Agency (Barantin) officers, scheduling a joint physical inspection rather than disconnected sequential reviews15.  
Red Channel containers are transferred under bonded custody from terminal yards via internal transfer trucks to the Tempat Pemeriksaan Fisik Terpadu (TPFT) Graha Segara17. At TPFT Graha Segara, containers pass through high-energy non-intrusive container scanning portals (G-Scan X-ray) or are positioned at covered longroom inspection docks11. Consignee representatives unseal the container, and labor teams destuff cargo under the joint supervision of customs examiners and quarantine officers11. Following verification, the inspector logs the digital inspection report (Berita Acara Pemeriksaan \- BAP) in CEISA 4.0, which releases the electronic SPPB10.

### **Phase 6: Hinterland Movement and Landside Gate Release via Highway Drayage**

Consignees extracting cargo via highway transport settle Terminal Handling Charges (THC), lift-on/lift-off (Lo-Lo) fees, and storage tariffs through Pelindo’s centralized billing portal, receiving an electronic Delivery Order (e-DO) and Container Delivery Ticket (Surat Penyerahan Petikemas \- SP2)10. Trucking operators register vehicles within the Port Authority’s Single Truck Identification Data (STID) framework and book collection appointments through the Terminal & Truck Booking System (TTBS/TBS)3.  
Upon arriving at the terminal, the external truck approaches the automated gate complex5. The Auto Gate System reads the truck’s passive RFID transponder, high-speed OCR cameras scan the front license plate and container numbers, and weigh-in-motion platforms measure gross axle loads4. The gate system checks these readings against the TOS, CEISA (for SPPB clearance), and STID records4. Once validated, the system prints an electronic interchange job slip, retracts the automated barrier, and assigns the driver to a designated yard bay10. An RTG loads the container onto the external chassis, and the vehicle exits through outbound Auto Gate portals that verify container identity and weight tolerances before final release into regional road corridors10.

### **Phase 7: Hinterland Movement via Multimodal Rail Corridors**

For freight moving to manufacturing districts in West and Central Java, cargo can be evacuated over intermodal rail links managed by PT Kereta Api Logistik (KAI Logistik / KALOG), a subsidiary of state railway operator PT Kereta Api Indonesia1. The primary rail connections operate out of the Pasoso Rail Terminal and the specialized on-dock rail siding at JICT1.  
Containers designated for rail routing are cleared at the port or moved under bonded transit declarations (Pemberitahuan Pindah Lokasi Penimbunan \- PLP) to inland dry ports, primarily Cikarang Dry Port (CDP / Lemahabang) or the Gedebage Rail Terminal in Bandung25. Terminal prime movers dray containers from terminal storage blocks over port internal corridors to the Pasoso or JICT siding23. Reach stackers and rail-mounted gantries load the containers onto specialized container flatcars (Gerbong Datar)30. Trains operate in consists of 30 to 60 wagons, hauling between 60 and 120 TEUs per trip31. Because trains share track corridors with the commuter rail network (KRL Jabodetabek), freight departures are concentrated during nighttime windows to avoid commuter congestion25.

## **2\. Integrated Process Map and Operational Governance Matrix**

The matrix below maps the operational stages of container processing across Tanjung Priok, detailing the responsible stakeholders, governing platforms, physical and documentary handoff requirements, operational benchmarks, and systemic constraints.

| Operational Stage | Primary Stakeholders | Governing Systems | Handoff Criteria | Target Performance Indicators | Common Bottlenecks | Systemic Dependencies |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **1\. Pre-Arrival & Berth Planning** | Shipping Line Agents, Terminal Vessel Planners, Tanjung Priok Port Authority (OP)1 | Inaportnet, Terminal Operating System (TOS), BAPLIE EDI1 | Approval of PPK/PKK; BAPLIE EDI ingested into TOS with validated stowage profile7. | Berth Assignment Variance: 0 hrs; Planning Horizon: \>24 hrs prior to ETA1. | Late submission of inward manifests; EDI parsing failures due to non-standard message formatting. | Dependent on timely vessel position feeds (AIS) and prompt customs manifest approvals (RKSP/BC 1.1). |
| **2\. Harbor Transit & Berthing** | Harbour Master (KSOP), Pelindo Marine Services (Pilots, Tugs)1 | Inaportnet, VTMS, Pelindo Marine Operating System (MOS)7 | Pilot boarded at outer station; line handling secured; KSOP clearance issued1. | Pilot Boarding Delay: \<30 mins; Berthing Approach Speed: \<0.15 m/s8. | Surge vessel arrivals at breakwater; tug dispatch delays during tidal crests; poor visibility or squalls. | Channel availability (150 m width constraints); basin clear zones; marine pilot availability1. |
| **3\. Quayside Unloading (STS)** | Terminal Operations, Stevedoring Companies (TKBM)7 | TOS Quayside Module, SIMON TKBM7 | Container off vessel deck; SATL twistlocks detached; physical tally reconciled in TOS7. | Gross Crane Moves/Hour (GMPH): 25–30 moves; Berth Moves/Hour (BMPH): \>60 moves. | Shortages in TKBM gang rotations; mechanical spreader failures; unlashing delays on deck. | Crane spreader availability; internal terminal truck availability under the crane hook. |
| **4\. Yard Stacking & Allocation** | Terminal Yard Control, Equipment Operators (RTG/ASC)10 | TOS Yard Module, DGPS/PDS Telemetry | Container landed in assigned ground slot; spatial coordinates updated in TOS database10. | Shifting/Reshuffle Ratio: \<0.15 reshuffles per retrieval; YOR Target: 60%–70%13. | Yard congestion when YOR \> 75%; RTG equipment breakdowns; truck queueing in narrow yard lanes10. | Internal truck cycle times; accuracy of pre-marshalling algorithms in the TOS. |
| **5\. Customs, Quarantine & Inspection** | DJBC (Bea Cukai), Barantin, PPJK/Importer, TPFT Operator10 | CEISA 4.0, INSW, SSm QC, TPFT Engine7 | Issuance of electronic SPPB; completion of joint inspection BAP at TPFT10. | Green Channel: \<24 hrs; Red Channel: 3–5 days; Joint Inspection Lead Time: \<48 hrs10. | Late preparation of goods by importers; inspection bay shortfalls at TPFT; slow quarantine lab results19. | Continuous uptime of CEISA 4.0-INSW API pipelines; prompt physical drayage to TPFT Graha Segara17. |
| **6\. Gate-Out Drayage (Road)** | Logistics Carriers, Terminal Gate Operators, Port Police4 | STID, Auto Gate System, TTBS, e-DO / SP23 | Real-time match of STID RFID, container OCR, and valid SPPB/SP2; barrier lift4. | Truck Round Time (TRT): \<45 mins; Gate Cycle Time: \<45 secs per vehicle3. | Manual exceptions from OCR read errors; missing STID credentials; long queues on port access corridors3. | High availability of external carrier networks; stability of gate OCR hardware; clear arterial road flow. |
| **7\. Intermodal Rail Dispatch** | PT KAI, KAI Logistik (KALOG), Terminal Rail Ops1 | KALOG Systems, Terminal Rail Module, CEISA (PLP)7 | Containers secured on flatcar chassis; train consist data validated; manifest dispatched30. | Rail Dispatch Schedule Adherence: \>95%; Train Turnaround: \<4 hrs. | Drayage bottlenecks between JICT stacks and Pasoso rail siding; curfew conflicts with KRL commuter trains25. | Commuter rail track windows; availability of flatcar rolling stock; double-handling drayage capacity23. |

## **3\. Systemic Bottlenecks, Regulatory Latencies, and Intermodal Dependencies**

### **Yard Occupancy Ratio Threshold Dynamics and Reshuffling Penalties**

The primary physical bottleneck within Tanjung Priok stems from the strict spatial constraints of the container yards across JICT, TPK Koja, and NPCT11. While international port engineering standards identify 60% to 70% as the sustainable Yard Occupancy Ratio (YOR) ceiling, operational surges regularly push local density beyond 75%10. As yard density crosses this threshold, rehandling penalties grow rapidly according to the relationship:  
![][image1]  
When YOR climbs past 75%, RTGs must divert time from loading outbound trucks to reshuffling top-tier containers to access buried boxes scheduled for release10. This rehandling slows down yard operations, causing internal drayage trucks to back up along yard access lanes. The congestion eventually extends back to the berth, leaving STS cranes idling while waiting for empty chassis, lowering gross crane moves per hour (GMPH), and extending vessel stays at berth.

### **Landside Congestion, STID Compliance, and Hinterland Road Bottlenecks**

Landside container movement faces significant traffic pressure, with over 15,000 trucks entering and leaving the port daily2. The automated gate systems and Single Truck Identification Data (STID) framework have reduced routine gate transactions to seconds, but physical queues remain an issue4. Dirty containers, damaged plates, or missing STID cards frequently cause OCR failures, forcing trucks into manual exception lanes and backing up traffic onto entry ramps21.  
This congestion is exacerbated by regional freight patterns. More than 60% of all containerized traffic entering and leaving Tanjung Priok travels to or from industrial corridors east of Jakarta—primarily Cibitung, Cikarang, and Karawang3. However, the port’s dedicated truck parking buffer areas are located along its western boundary3. Lacking convenient parking near their travel routes, drivers often stage along port access roads such as Jalan Jampea, Jalan Cakung-Cilincing, and access points to the elevated toll road3. These informal queues spill back into terminal entrances, pushing average Truck Round Times (TRT) well past target thresholds3.

### **Customs Clearance Latencies and Examination Protocols**

While port dwell times have improved from historical highs of over seven days down toward targets of three to four days, the pre-clearance phase still accounts for the largest share of cargo dwell time13. Many importers and clearing agents wait until a vessel has berthed before submitting their Import Declarations (PIB), forfeiting the opportunity to clear documentation while cargo is still at sea10.  
For cargo flagged for physical inspection (SPJM), transferring containers across port service roads to TPFT Graha Segara creates an operational chokepoint17. Containers must be moved under bonded customs transit, processed through X-ray scanning tunnels, and brought into inspection bays11. While the Single Submission Quarantine Customs (SSm QC) platform coordinates joint inspections between customs and quarantine authorities, delays remain common15. Delays are driven by backlogs at longroom inspection docks, laboratory testing turnarounds for agricultural goods, and missing importer representatives required to witness container unsealing11.

### **Intermodal Rail Siding Constraints and Urban Track Sharing**

Despite direct rail access at JICT and the nearby Pasoso station, rail handles only a small portion of the port's total container volumes1. The primary obstacle is the cost of double-handling10. Most berths lack direct track access beneath the STS crane tracks1. As a result, containers must be moved from the quay to a yard stack, and later transferred again over internal roads to the rail siding, incurring extra handling fees and equipment moves that reduce rail's cost advantage over highway drayage10.  
Rail capacity is also restricted by scheduling conflicts on the mainline network25. Freight trains running between Tanjung Priok and inland hubs like Cikarang Dry Port or Gedebage share tracks with the commuter rail system (KRL Jabodetabek)25. Commuter services take priority during the day, restricting freight trains to narrow daytime windows and overnight hours25. This cap on rail operations limits the port's ability to shift inland freight off congested road corridors.

## **4\. Field Audit Program: Ten Operational Observations for the K36 Inspection**

The K36 inspection team should conduct targeted observations across critical operating areas, using the following checkpoints to assess equipment performance, interface synchronization, and process compliance:

### **1\. STS Gantry Duty Cycle Efficiency and Apron Under-Spreader Dwell**

* **Location**: Quayside Berth Apron (JICT, NPCT1, or TPK Koja)1.  
* **Observation Focus**: Monitor STS crane cycle times across twenty consecutive container discharges.  
* **Audit Methodology**: Measure time spent during hoisting, trolley travel, positioning, and spreader unlock. Record idle spreader time hovering over the quay apron while waiting for internal drayage trucks to position. A recurring delay exceeding 15 seconds points to truck shortages or yard dispatching issues. Confirm that SATL twistlock removal happens promptly on the deck without delaying crane lift cycles.

### **2\. Yard Corridor Drayage Traffic and Internal Truck Queue Density**

* **Location**: Terminal Internal Circulation Corridors and Block Turning Intersections.  
* **Observation Focus**: Traffic movement and queuing of internal terminal tractors.  
* **Audit Methodology**: Observe whether internal trucks move continuously or bunch up at block entrances. Note occurrences of "tractor pooling," where three or more tractors wait idle outside a single yard block. This pooling indicates an RTG delayed by container reshuffles or communication lags within the TOS dispatch engine.

### **3\. RTG Handling Operations, Reshuffle Activity, and Cab Telemetry Usage**

* **Location**: Active Import Stacking Blocks.  
* **Observation Focus**: Yard crane productivity and the proportion of non-productive handling moves.  
* **Audit Methodology**: Count non-productive container reshuffles against productive box loads onto external trucks over a two-hour window. Verify whether RTG operators use their in-cab Position Detection System (PDS) displays to locate containers, or if they rely on manual yard checks over radio channels. Check e-RTG power connections (busbar or cable reels) for wear or maintenance issues.

### **4\. Inbound Auto Gate OCR Read Rates and Exception Lane Processing**

* **Location**: Inbound Terminal Gate Complex5.  
* **Observation Focus**: Optical Character Recognition reliability and driver interventions4.  
* **Audit Methodology**: Track transactions across automated gate lanes, recording the time from truck entry on the scale to barrier arm release (benchmark: under 45 seconds)21. Note how often drivers must exit their cabs to reposition chassis, swipe cards, or contact support. Tally how many trucks are diverted to manual exception bays due to OCR misreads, database timeouts, or document errors4.

### **5\. Single Truck Identification Data Card Verification and Bypass Practices**

* **Location**: Gate Kiosks and Exception Handling Stations4.  
* **Observation Focus**: Enforcement of the port authority's STID compliance rules4.  
* **Audit Methodology**: Observe how gate clerks handle trucks arriving with damaged, expired, or non-compliant STID credentials4. Check whether clerks turn away non-compliant trucks or issue manual passes. High manual override rates undermine gate tracking accuracy and weaken port security data.

### **6\. Cold-Chain Monitoring Practices and Reefer Gantry Utilization**

* **Location**: Dedicated Reefer Yard Stacking Areas11.  
* **Observation Focus**: Electrical hookup management and temperature log integrity11.  
* **Audit Methodology**: Inspect reefer gantry towers to assess socket usage, grounding cables, and cable wear11. Observe technicians taking temperature readings, noting whether they log data digitally with mobile devices or record it manually on paper. Check for reefer containers left on trailers or staged in general stacks without power, assessing risks of temperature abuse.

### **7\. Bonded Drayage Transfers to TPFT Graha Segara and Non-Intrusive Inspection (G-Scan)**

* **Location**: Customs Transfer Route to TPFT Graha Segara and Inspection Intake17.  
* **Observation Focus**: Movement of Red Channel containers and non-intrusive scanning flow10.  
* **Audit Methodology**: Follow the transit of containers moving under bonded transfer status (PLP) from terminal stacks into the TPFT Graha Segara facility17. Track truck waiting times at the G-Scan drive-through X-ray portal11. Determine whether scanning flows smoothly or creates truck queues that back up onto port roads.

### **8\. Joint Customs and Quarantine Physical Inspection Protocols at Examination Sheds**

* **Location**: TPFT Graha Segara Covered Longroom Examination Docks11.  
* **Observation Focus**: Single Submission Quarantine Customs (SSm QC) inter-agency coordination15.  
* **Audit Methodology**: Watch physical container examinations along the longroom platform11. Confirm whether customs officers and quarantine examiners inspect cargo simultaneously as envisioned under SSm QC, or conduct sequential reviews15. Record time lost waiting for clearing agents (PPJK) or warehouse labor to arrive and open containers19.

### **9\. Intermodal Rail Transfer Operations at Pasoso Station and JICT Rail Siding**

* **Location**: Pasoso Rail Yard and JICT On-Dock Rail Spur1.  
* **Observation Focus**: Efficiency of container handling between trucks, yards, and rail wagons23.  
* **Audit Methodology**: Observe reach stackers and cranes loading containers onto KAI Logistik flatcars25. Record average lift cycle times per wagon and note any prolonged idle periods. Identify whether containers are transferred directly from terminal haulers or staged in intermediate stacks, noting points where double-handling adds costs and delays.

### **10\. Apron Occupational Safety, Traffic Separation, and Container Stack Integrity**

* **Location**: Quayside Apron, Yard Corridors, and Primary Terminal Intersections.  
* **Observation Focus**: Safety enforcement, traffic management, and yard physical conditions.  
* **Audit Methodology**: Check whether stevedores, unlashing crews, and tally clerks stay within marked safety zones and wear required safety gear (PPE). Look for foot traffic crossing active RTG travel lanes or walking beneath suspended crane spreaders. Inspect yard stacks for leaning containers, damaged corner castings, or structural defects that could present safety risks.

## **5\. Evidence-Based Inquiries for Terminal Operators and Authority Leadership**

The audit team should present the following data-focused questions to senior leadership at Pelindo Regional 2, terminal operating companies (JICT, TPK Koja, NPCT1), customs units, and intermodal transport providers:

### **Marine Services, Berth Productivity, and Quayside Performance**

* What is the monthly average difference between scheduled vessel arrival times and actual berthing, and how many hours are lost to pilotage delays, tug availability, or channel navigation issues1?  
* What are your current performance targets versus actual figures for Gross Crane Moves Per Hour (GMPH) and Berth Moves Per Hour (BMPH) across different vessel classes, and what portion of lost crane time is attributable to machinery breakdowns, weather delays, or stevedoring gang handoffs?  
* How does your Terminal Operating System manage mid-operation stowage changes or unexpected draft discrepancies without causing crane idle time along the berth?

### **Yard Density, Reshuffling Intensity, and Dwell-Time Governance**

* What is your daily Yard Occupancy Ratio (YOR) profile across each terminal block, and what operational triggers are used to divert inbound containers to off-dock yards when storage density exceeds 75%10?  
* What is the terminal's measured non-productive reshuffle ratio per container retrieval, and what proportion of RTG operating hours is spent moving blocking containers13?  
* How are progressive storage tariffs structured and enforced to discourage shippers from using terminal yards for cheap interim storage, and what volume of containers exceeds 14 days of dwell time each month10?

### **Gate Automation, STID Compliance, and Road Traffic Integration**

* What is the first-pass success rate of your Auto Gate OCR cameras for reading container codes and vehicle license plates, and what percentage of trucks must be diverted to manual exception bays weekly4?  
* How does the terminal coordinate with the Port Authority (OP Priok) and traffic police when gate queues begin backing up onto arterial access roads and toll corridors3?  
* What proportion of active drayage trucks has fully registered STID tags, and what automated controls prevent drivers from sharing RFID tags among unregistered vehicles3?

### **Customs, Quarantine, and Multi-Agency Digital Integration**

* Since rolling out the Single Submission Quarantine Customs (SSm QC) platform, what is the verified average time from when a Red Channel notice is issued to when physical inspection starts at TPFT Graha Segara15?  
* What are your documented uptime statistics for the API interfaces connecting the terminal's TOS, CEISA 4.0, and the LNSW platform, and what backup procedures protect gate and yard operations during system outages7?  
* What percentage of containers flagged for Red Channel inspection complete destuffing, examination, and resealing within a 24-hour window, and what are the primary causes of inspection backlogs19?

### **Intermodal Rail Connections and Inland Port Development**

* What is the current volume split between road trucking and KAI Logistik (KALOG) rail services for containerized freight moving to industrial corridors in West Java23?  
* What are the comparative end-to-end handling costs and cycle times for containers cleared via Cikarang Dry Port (CDP) versus cargo moving by direct road transport through Tanjung Priok's gates10?  
* How are terminal operators, PT KAI, and the Ministry of Transportation working to secure additional daytime rail freight windows along the shared commuter rail network to expand intermodal capacity1?

## **6\. Strategic Synthesis and Systemic Evaluation**

Optimizing container flows through the Port of Tanjung Priok requires balancing digital system integration with the physical capacity of port infrastructure. Significant progress has been made in coordinating regulatory and administrative workflows through digital systems such as Inaportnet for vessel movements, CEISA 4.0 for customs declarations, the National Logistics Ecosystem (NLE) for supply chain data, and the Single Truck Identification Data (STID) framework for vehicle access3.  
However, physical handling and spatial constraints remain the primary source of cargo delays. High container yard density (YOR exceeding 75%) causes excessive container reshuffling, truck traffic is concentrated along a single eastern highway corridor, and rail intermodal transport requires costly double-handling3. Addressing these challenges requires terminal operators and port authorities to focus on four operational priorities:  
First, gate and yard flows should be synchronized by enforcing mandatory Terminal & Truck Booking System (TTBS) appointment windows tied directly to verified STID tags3. Limiting hourly gate appointments to match available yard crane capacity will help eliminate truck queuing along port access roads and stabilize truck turnaround times3.  
Second, intermodal rail operations require streamlined handling arrangements. Pelindo, terminal operators, and PT KAI should establish dedicated, bonded transfer corridors between quayside berths and the Pasoso rail siding1. Reducing extra handling steps and tariffs will help make rail transport cost-competitive with highway drayage for cargo moving to industrial centers in West Java10.  
Third, terminals should enforce strict yard clearance rules to keep occupancy below 70%13. Moving import containers that have exceeded three days of dwell time to off-dock bonded inland depots (PLP sites) will free up space in prime terminal yards, reduce non-productive rehandling, and maintain steady discharge rates at the quayside13.  
Finally, customs and quarantine authorities must continue strengthening joint inspection procedures at TPFT Graha Segara under the Single Submission Quarantine Customs (SSm QC) platform15. Setting clear response deadlines for clearing agents and speeding up laboratory testing turnarounds will help reduce physical examination delays, ensuring the terminal complex can support continued trade growth across the region15.

#### **Works cited**

> 1. 2.1.1 Indonesia Jakarta Port of Tanjung Priok, [https://lca.logcluster.org/211-indonesia-jakarta-port-tanjung-priok](https://lca.logcluster.org/211-indonesia-jakarta-port-tanjung-priok)  
> 2. Port of Tanjung Priok: Jakarta Port Guide & IDTPP Code, [https://www.freightamigo.com/en/blog/logistics/port-of-tanjung-priok-indonesias-busiest-jakarta-port-and-global-trade-gateway/](https://www.freightamigo.com/en/blog/logistics/port-of-tanjung-priok-indonesias-busiest-jakarta-port-and-global-trade-gateway/)  
> 3. Priok Path toward TTBS Adoption \- The Shipping Gazette, [https://theshippinggazette.com/priok-path-toward-ttbs-adoption/](https://theshippinggazette.com/priok-path-toward-ttbs-adoption/)  
> 4. Analisis Penggunaan STID Pada Pelabuhan Auto Gate System, [https://jurnal.peneliti.net/index.php/JIWP/article/download/9639/7655/](https://jurnal.peneliti.net/index.php/JIWP/article/download/9639/7655/)  
> 5. Analyzing The Impact of Gate Automation To Expedite Export Import, [https://proceedings.itltrisakti.ac.id/index.php/ATLR/article/download/155/188](https://proceedings.itltrisakti.ac.id/index.php/ATLR/article/download/155/188)  
> 6. Go Live \- PT IPC Terminal Petikemas, [https://ipctpk.co.id/wp-content/uploads/2020/10/AR-IPC-TPK-2018.pdf](https://ipctpk.co.id/wp-content/uploads/2020/10/AR-IPC-TPK-2018.pdf)  
> 7. OP Priok Kembali Tekankan Optimalisasi Program Digitalisasi, [https://maritimnews.com/2022/07/op-priok-kembali-tekankan-optimalisasi-program-digitalisasi-pelabuhan/](https://maritimnews.com/2022/07/op-priok-kembali-tekankan-optimalisasi-program-digitalisasi-pelabuhan/)  
> 8. 16 14-C-1 Objective Ship Size for Tanjung Priok Port 59\. The, [https://openjicareport.jica.go.jp/pdf/11744273\_04.pdf](https://openjicareport.jica.go.jp/pdf/11744273_04.pdf)  
> 9. Tanpa Buffer Area, Penerapan TBS Bakal Munculkan Problem Baru, [https://oceanweek.co.id/tanpa-buffer-area-penerapan-tbs-bakal-munculkan-problem-baru/](https://oceanweek.co.id/tanpa-buffer-area-penerapan-tbs-bakal-munculkan-problem-baru/)  
> 10. Professional cargo handling at Tanjung Priok port Indonesia, [https://gf-lines.com/en/articles/professional-cargo-handling-at-tanjung-priok-port-indonesia/](https://gf-lines.com/en/articles/professional-cargo-handling-at-tanjung-priok-port-indonesia/)  
> 11. Facilities Info \- Jakarta \- Graha Segara, [https://www.grahasegara.co.id/gs/facilities\_info](https://www.grahasegara.co.id/gs/facilities_info)  
> 12. Evaluation of Container Terminal Efficiency Performance in Indonesia, [https://thesis.eur.nl/pub/33021/Syafaaruddin-D.S.-Evaluation-of-container-terminal-efficiency-performance-in-Indonesia-Future-Investment.pdf](https://thesis.eur.nl/pub/33021/Syafaaruddin-D.S.-Evaluation-of-container-terminal-efficiency-performance-in-Indonesia-Future-Investment.pdf)  
> 13. (PDF) Evaluasi Penurunan Dwelling Time Menjadi Empat Hari Di, [https://www.researchgate.net/publication/329839301\_Evaluasi\_Penurunan\_Dwelling\_Time\_Menjadi\_Empat\_Hari\_Di\_Pelabuhan\_Tanjung\_Priok](https://www.researchgate.net/publication/329839301_Evaluasi_Penurunan_Dwelling_Time_Menjadi_Empat_Hari_Di_Pelabuhan_Tanjung_Priok)  
> 14. Evaluasi Progres Pelabuhan Banjarmasin | PDF \- Scribd, [https://id.scribd.com/document/739466254/RAPAT-EVALUASI-B-15-PELABUHAN-BANJARMASIN-pdf](https://id.scribd.com/document/739466254/RAPAT-EVALUASI-B-15-PELABUHAN-BANJARMASIN-pdf)  
> 15. Single Submission, Sistem Kolaborasi yang Menghadirkan Solusi, [https://klc2.kemenkeu.go.id/storage/kms/document/2024/1/31/1706693655724rhx/SSM%20-%20Mini%20Artikel.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256\&X-Amz-Credential=userklc2/20260927/us-east-1/s3/aws4\_request\&X-Amz-Date=20260927T144106Z\&X-Amz-Expires=25200\&X-Amz-SignedHeaders=host\&X-Amz-Signature=57c785b630fd821a37a5b30fc8a6fca90e9ff978e592a90132a03aeb494e79f3](https://klc2.kemenkeu.go.id/storage/kms/document/2024/1/31/1706693655724rhx/SSM%20-%20Mini%20Artikel.pdf?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=userklc2/20260927/us-east-1/s3/aws4_request&X-Amz-Date=20260927T144106Z&X-Amz-Expires=25200&X-Amz-SignedHeaders=host&X-Amz-Signature=57c785b630fd821a37a5b30fc8a6fca90e9ff978e592a90132a03aeb494e79f3)  
> 16. Analysis of the National Logistics Ecosystem Program in Increasing, [https://proceedings.itltrisakti.ac.id/index.php/ATLR/article/download/731/770](https://proceedings.itltrisakti.ac.id/index.php/ATLR/article/download/731/770)  
> 17. About Us \- Graha Segara, [https://www.grahasegara.co.id/gs/about](https://www.grahasegara.co.id/gs/about)  
> 18. NLE making logistics processes simpler: minister \- ANTARA News, [https://en.antaranews.com/news/270660/nle-making-logistics-processes-simpler-minister](https://en.antaranews.com/news/270660/nle-making-logistics-processes-simpler-minister)  
> 19. News \- Graha Segara, [https://www.grahasegara.co.id/gs/berita\_detail.php?id=d2xhbTgrVXdrcFJPdHRQV0crakhhdz09](https://www.grahasegara.co.id/gs/berita_detail.php?id=d2xhbTgrVXdrcFJPdHRQV0crakhhdz09)  
> 20. Tanjung Priok: Bea Cukai Optimalkan Pemeriksaan Fisik Peti Kemas, [https://muc.co.id/id/article/tanjung-priok-bea-cukai-optimalkan-pemeriksaan-fisik-peti-kemas](https://muc.co.id/id/article/tanjung-priok-bea-cukai-optimalkan-pemeriksaan-fisik-peti-kemas)  
> 21. penerapan single truck identification data dalam kelancaran arus, [http://repository.poltekpel-sby.ac.id/654/1/Yunita%20Putri%20Dwilestari%20-%20Halaman%20Awal%20Bab%20I%2C%20II%20%26%20III.pdf](http://repository.poltekpel-sby.ac.id/654/1/Yunita%20Putri%20Dwilestari%20-%20Halaman%20Awal%20Bab%20I%2C%20II%20%26%20III.pdf)  
> 22. ID Laporan Keberlanjutan Tahun 2025 1 \- pdfcoffee.com, [https://pdfcoffee.com/id-laporan-keberlanjutan-tahun-2025-1-pdf-free.html](https://pdfcoffee.com/id-laporan-keberlanjutan-tahun-2025-1-pdf-free.html)  
> 23. Action Programme on Intermodal Freight Transport in Java, Indonesia, [https://changing-transport.org/wp-content/uploads/2021\_Action-Programme-on-Intermodal-Freight-Transport-in-Java-Indonesia-1.pdf](https://changing-transport.org/wp-content/uploads/2021_Action-Programme-on-Intermodal-Freight-Transport-in-Java-Indonesia-1.pdf)  
> 24. PT Kereta Api Logistik Annual Report Laporan Tahunan 2017, [https://kailogistik.id/public/uploads/document/annual-report/6\_annual\_20200109182402.pdf](https://kailogistik.id/public/uploads/document/annual-report/6_annual_20200109182402.pdf)  
> 25. Mulai 14 Januari, Kereta Peti Kemas Gedebage-Tanjung Priok, [https://finance.detik.com/berita-ekonomi-bisnis/d-3395580/mulai-14-januari-kereta-peti-kemas-gedebage-tanjung-priok-jalan-2-kali-hari](https://finance.detik.com/berita-ekonomi-bisnis/d-3395580/mulai-14-januari-kereta-peti-kemas-gedebage-tanjung-priok-jalan-2-kali-hari)  
> 26. Final Report on Project for Master Plan Study on Port Development, [https://openjicareport.jica.go.jp/pdf/12068581\_01.pdf](https://openjicareport.jica.go.jp/pdf/12068581_01.pdf)  
> 27. Dampak Dwelling Time Terhadap Layanan Ekspor Impor di, [https://ejurnal.polimarin.ac.id/index.php/jmp/article/download/12/2/80](https://ejurnal.polimarin.ac.id/index.php/jmp/article/download/12/2/80)  
> 28. www.bphn.go.id, [https://bphn.go.id/data/documents/10pmhub015.pdf](https://bphn.go.id/data/documents/10pmhub015.pdf)  
> 29. laporan tahunan 2022annual report \- KAI Logistik, [https://kailogistik.id/public/uploads/document/annual-report/11\_annual\_20230802103018.pdf](https://kailogistik.id/public/uploads/document/annual-report/11_annual_20230802103018.pdf)  
> 30. KAI Tambah Rute Angkutan Kontainer ke Semarang \- Liputan6.com, [https://www.liputan6.com/bisnis/read/2606676/kai-tambah-rute-angkutan-kontainer-ke-semarang](https://www.liputan6.com/bisnis/read/2606676/kai-tambah-rute-angkutan-kontainer-ke-semarang)  
> 31. Kereta Logistik di Priok Mampu Angkut 120 Kontainer per Hari, [https://ekbis.sindonews.com/berita/1086333/34/kereta-logistik-di-priok-mampu-angkut-120-kontainer-per-hari](https://ekbis.sindonews.com/berita/1086333/34/kereta-logistik-di-priok-mampu-angkut-120-kontainer-per-hari)  
> 32. Kantor Otoritas Pelabuhan Tanjung Priok Percepat NLE Di, [https://mimbarmaritim.com/2022/07/14/kantor-otoritas-pelabuhan-tanjung-priok-percepat-nle-di-pelabuhan-melalui-pelayanan-berbasis-digital/](https://mimbarmaritim.com/2022/07/14/kantor-otoritas-pelabuhan-tanjung-priok-percepat-nle-di-pelabuhan-melalui-pelayanan-berbasis-digital/)  
> 33. Study of Container Dwelling Time in Indonesia: Current Condition, [https://www.researchgate.net/publication/332417339\_Study\_of\_Container\_Dwelling\_Time\_in\_Indonesia\_Current\_Condition\_Challenge](https://www.researchgate.net/publication/332417339_Study_of_Container_Dwelling_Time_in_Indonesia_Current_Condition_Challenge)  
> 34. Purbaya Sidak 3.100 Kontainer Menumpuk di Tanjung Priok \- Tirto.id, [https://tirto.id/purbaya-sidak-3100-kontainer-menumpuk-di-tanjung-priok-hxr5](https://tirto.id/purbaya-sidak-3100-kontainer-menumpuk-di-tanjung-priok-hxr5)  
> 35. Sambutan \- INSW, [https://api.insw.go.id/assets/upload/cms/1717158165864\_cms.pdf](https://api.insw.go.id/assets/upload/cms/1717158165864_cms.pdf)  
> 36. Reducing External Container Trucks' Turnaround Time in Ports, [https://www.researchgate.net/publication/365055252\_Reducing\_External\_Container\_Trucks'\_Turnaround\_Time\_in\_Ports\_A\_Data-driven\_Approach\_under\_Truck\_Appointment\_Systems](https://www.researchgate.net/publication/365055252_Reducing_External_Container_Trucks'_Turnaround_Time_in_Ports_A_Data-driven_Approach_under_Truck_Appointment_Systems)  
> 37. NPCT1 Records Brilliant Performance, Exceeding 10 Million TEUs, [https://www.islnewstv.com/2025/12/npct1-records-brilliant-performance.html](https://www.islnewstv.com/2025/12/npct1-records-brilliant-performance.html)

[image1]: <data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAmwAAABACAYAAACnZCtBAAAEyElEQVR4Xu3dS6itYxgH8FcoIpcUuV86EyEkSmEgCmGAjsuEicvAgJAyMlGEExISiSIpMiJSdmYu04NccsklhAyYubz/vu+zvvVaZy/22Tlrr/P71dNa61lfa6+99+Tfe/tKAQAAAAAAAAAAAAAAAAAAAAAAAAAAAACWxq61NrdNAAAWw0W1vq71a/sGAACL4/YisAEALDSBDQBgwQlsAAALTmADAFhwAhsAwIJLYPutbQIAsBier/VnX9/U2jL9NgDA2u1S6+xa39d6staLtU6s9db4IgAAdox9a/1c67Smv7XWQ00PAIAd4IFal7fNaqXWJW0TAID/126lW281y/6luy/metuvf9x7qvvvJEB+Wrqp2wvLZCr3s1rnj64DAFgah9b6sW2uwV2lu4/mahKubq71Sa1zaj1a65daT48vmiPr6zKFu2et32tdWuvtWseOLwIAWCanlG7qs5VwtaltzjEvsOVnvdw/H67N438JbPmMwcmlW3u316gHALB09ihd6GndP3r+Qa2zah1R68zShbkbS3feWJzbPz5Xa/da7/SvM32Zac/0EsxWC2wJX6/UOqDW8f17s4xDYdbdvVHro1pHjvoAAEunHaXap0xvNhhGwM6odW2ty/reFbWeLZN1bkOAW+kfE66GdWrzAlumVHOESD57tZG6R0o3JRrvl+7okXz/d/++Yr61rJ1bNFlfmOAMAOxEsgYsYemQ8s8gMAS2g2qd3j/PAv+Et3i4f9xWYEvNC2znlcmZbyf0j9uSgDhsXBg7sG3M8Gat45re5lpHNb21uKFMDs39atTPJomhP7iy1uOlC715/4XRe+PPyeG7Wav3Wpn+v2TU8pnRawBgJ3ZS6XZg3t2/TuC5rnQjWzeVLnBkSvT6Wu/Vuqp099FMoDqs1jWl22jwYemmTH+qdUGt12vd2z/+ULoRvltqXV0mI2jrLYHnztHrbFx4sHTfd7w2bnvkb/FxrcNHvUwlJ5AOgSthK3+HQb7HE2V6WveOMgl4uT7hOJs08nyQqePxzwEA2PAyApg1e631DGyRUbHxusCE0kFGKbMmMLtzW+MRuHzX9riVvH6s6WUqONOjAABL4Yu20VvvwJaNE9l4kU0R2aSREbTBrCA2yA3jE+hifF2mgDOFel+ZHmGL/E4ONwYAlsZ3baO33oEtMjX6ZenOiBvLer1tBbZ8j4P750NgWyndGrasc2vXFsZKmawdBADY8BKgZlktsGXtXjYHzKp5d1ZI4Gp3vF7c92ftVE1/2K3bjsRljeCsYLZSuvVvAABLYS2BbXvMCmxHl24H6TFNP6Nnq61hy+fkCJV2lG2lzA5yAAAb0ta20cvasVPb5jpI4JoVprIObbwpIbticwBwduQOxrtEI2fgfVu6oDfs2I1MleY2XwAAS+Gp5nWmH3O8RoJRasv022uWc9TGnzsrUOUIk5yjlmNRPq/10ui99hy2SMj7o3RHodzT9yIhdNaOUwCADSm7N3Me2rLI75NdqAAAS+W2vja6TbVebZsAAMsgU4u3ts0NKPdezZ0kAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA2Kn9BRUkxw4ONwSiAAAAAElFTkSuQmCC>