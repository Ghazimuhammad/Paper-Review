# Energy Efficiency of Open Radio Access Network: A Survey

## About

| Item | Information | 
| -------- | -------- | 
|Paper Link|https://ieeexplore.ieee.org/document/10200477|
|Authors|Attai Ibrahim Abubakar, Oluwakayode Onireti, Yusuf Sambo, Lei Zhang, G. K. Ragesh, Muhammad Ali Imran|
|Date of Publication|20-23 June 2023|
|Total Pages|7|
|Keywords|O-RAN, Energy Efficiency, Power Consumption Model, 5G and Beyond Networks.|

This paper, we investigate the O-RAN from an Energy efficiency (EE) perspective by reviewing the state-of-the-art power consumption models, and EE techniques that have been proposed to minimize the energy consumption of O-RAN. In addition, the challenges associated with the optimization of the EE of O-RAN and opportunities for further research are highlighted.

## Introduction
* The radio access network (RAN) has evolved from a distributed architecture to a centralized/cloud-RAN (C-RAN) and now to an open-RAN (O-RAN) architecture.
* The O-RAN architecture includes three network entities: Centralised Unit (CU), Distributed Unit (DU), and Radio Unit (RU), and uses open radio interfaces and virtualization of network functions.
* O-RAN facilitates cost savings, broadens the supply chain, enables network scalability, intelligent network management, efficient resource allocation, and reduced CAPEX/OPEX.
* The UK government has heavily invested in O-RAN development for the deployment of beyond 5G networks.
* The impact of O-RAN on energy consumption is still an area of open research.
* This paper investigates O-RAN's energy efficiency (EE) by reviewing power consumption models and techniques for improving EE.

## RAN Evolution
* Traditional RAN or Distributed RAN (D-RAN) architecture consists of a base station segmented into a BBU and RRH, with closed interfaces and limited inter-operation among different vendor equipment.
* Centralized-RAN (C-RAN) architecture pools BBUs in a central location, improving resource utilization, network scalability, coordination, load balancing, and energy efficiency.
* Virtual-RAN (V-RAN) architecture builds on C-RAN by introducing network virtualization, deploying BBUs as software on generic servers, improving flexibility, scalability, and reducing OPEX and CAPEX.
* O-RAN architecture separates the RAN into O-CU, O-DU, and O-RU nodes, disaggregates network functions, embraces virtualization, employs open interfaces, and includes intelligent controllers for AI and machine learning support.
* O-RAN enhances network deployment flexibility, dynamic resource allocation, and supports interoperability among different vendor hardware and software.

## Power Consumption of O-RAN
* O-RAN power consumption is mainly related to data processing in cloud or edge servers and data transportation through backhaul, midhaul, and fronthaul links.
* Power consumption components include RF transceivers, power amplifiers, CPUs, accelerators, cooling system, monitoring system, power supply, and more.

![image](https://hackmd.io/_uploads/By4qcQJpp.png)

* The power consumption of the radio network is determined by the hardware and software used in CUs, DUs, and RUs, as well as their location on the network nodes. Network virtualization in O-RAN leads to energy consumption in the radio unit due to computation overhead.
* Components of the radio network include CPUs, accelerators, network interface cards, RF transceivers, power amplifiers, and common site infrastructures.
* The energy consumption of the radio network depends on the functional split implemented, with more centralized network functions at the CU resulting in lower energy consumption of the RU.
* The power consumption of the transport network depends on technology, network configuration, capacity requirement, and the number of connections between CUs, DUs, and RUs. Components include switches, transponders, and multiplexers.
* The power consumption of the transport network also varies with the type of split option adopted, with lower functional splits leading to higher energy consumption due to increased capacity in the transport network.

## Energy Efficiency Techniques in O-RAN
* The literature on energy efficiency (EE) techniques in O-RAN can be classified into three categories: dynamic resource allocation and network function placement (DRA&NFP), dynamic location of DUs and CUs, and indirect EE optimization approaches.
* DRA&NFP focuses on segmenting processing operations between CUs and DUs to minimize energy consumption while meeting QoS requirements.
* 


