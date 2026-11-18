# Smart Home Energy: Model-Based Systems Engineering with SysML and Eclipse Arrowhead

A **SysML model** of an AI-driven smart-home energy system that reduces household energy use while
keeping the residents comfortable. It is designed as a service-oriented **System of Systems** on
the **Eclipse Arrowhead** framework and modelled in **Eclipse Papyrus**. Course: *IoT Automation*
(D7065E), Luleå University of Technology, 2025.

**Tools:** SysML · Eclipse Papyrus · Eclipse Arrowhead 5.0 (Service Registry, Orchestration, Authorization)

## The system

Sensors publish temperature, light and power measurements. An **AI trainer** learns from the
history, an **energy optimizer** produces an HVAC schedule, and an **HVAC controller** applies it.
The resident sets comfort preferences and follows consumption on a dashboard. All systems run in
one Arrowhead Local Cloud and find each other at runtime through service discovery, orchestration
and authorization, so they stay loosely coupled.

| Requirement | Description |
|---|---|
| F1–F4 | Collect Temp/Lux/Power, train a model on history, produce an optimized HVAC schedule, visualize consumption |
| N1 Security | Every service call needs an Authorization permit; consumers then connect to the provider over TLS |
| N2 Loose coupling | Discovery and late binding through Orchestration |
| N3 Resilience | Fall back to the last valid schedule when data is missing |

## Diagrams

| Use cases | Block definition diagram |
|---|---|
| ![Use cases](Diagrams/UC_SmartHomeEnergy.PNG) | ![BDD](Diagrams/BDD_SmartHomeEnergy.PNG) |

**Internal block diagram of the Local Cloud**

![IBD](Diagrams/IBD_LocalCloud.PNG)

## Documents

Written according to the Eclipse Arrowhead documentation structure:

- [`SoSD_SmartHomeEnergy.pdf`](Documents/SoSD_SmartHomeEnergy.pdf): System of Systems Description
- [`SySD_SmartHomeEnergy.pdf`](Documents/SySD_SmartHomeEnergy.pdf): System Description
- [`SD_SmartHomeEnergy.pdf`](Documents/SD_SmartHomeEnergy.pdf): Service Description

## Open the model

Import `WS-D7065E-2025/` as an Eclipse workspace with Papyrus and the SysML 1.6 profile installed.
The main model is `WS-D7065E-2025/D7065E-2025/D7065E-2025.di`. A browsable HTML export is in
`WS-D7065E-2025/D7065E-2025/D7065E-2025/index.html`.

## Author

**Abdalrahman Nasser**
