### IMTECO Ltd: Modelling the Hydrological Impact of Infrastructure Near Bog Pool Systems

**Partner**: Irene Tierney – Principal Ecologist, IMTECO Ltd  
**Email**: [irenetierney@imtecoltd.com](mailto:irenetierney@imtecoltd.com)  

---

#### Context & Motivation

Peatlands with **dense bog pool systems** are highly sensitive ecosystems. Infrastructure (e.g. wind farms, access tracks, buried cables) is usually prohibited in these zones — but even construction near the pools can affect their delicate **hydrology**. Impacts include drainage “shadows”, altered connectivity between pools, or changes in hydroperiod (pool water duration and levels).

Currently, there is **no standard tool** for ecologists or regulators to quantify these risks or to define *evidence-based buffer zones*, as is done for other sensitive habitats like GWDTEs (Groundwater-Dependent Terrestrial Ecosystems).

#### The Challenge

How can we **develop or adapt a hydrological modelling tool** that allows users (especially non-modellers like ecologists) to assess:

- How infrastructure might influence nearby **bog pool dynamics**.  

- What buffer zones are necessary to minimise hydrological disruption.  

- How to communicate these risks clearly to regulators and developers.  

The tool should be:

- Scientifically credible.   

- Flexible enough to incorporate field data.   

- Simple enough to be used in practical consultancy settings.   

#### Realistic Outcome for the Workshop

This is a **broad and ambitious challenge**. A fully working model cannot be built in two days — but this group aims to:

- Identify key physical processes and modelling options

- Review what tools already exist (and their limitations)

- Discuss the **data requirements** and simplifications needed for consultants

- Propose a **roadmap** for developing a prototype tool, e.g. in Python/R or an interface for an existing model (like DigiBog or HEC-RAS)

The result would be a shared vision and technical outline that could seed a collaborative research or innovation project.

---

#### Modelling Approaches (for discussion)

Below is a categorisation of possible modelling approaches, adapted from current research and industry practice. These should be discussed in terms of feasibility, input requirements, and applicability to bog pool systems.

---

**1. Physically-Based Distributed Flow Models (2D/3D)**  
Examples: **MIKE SHE**, **HydroGeoSphere**, **MODFLOW** (with UZF/SFR/LAK), **COMSOL**  

- Simulate: water-table response to tracks/foundations, pool water levels, GW–SW (groundwater–surface water) exchange, culvert placement  

- Inputs:  
  - High-resolution LiDAR digital elevation model (DEM)  

  - Peat layer stratigraphy and hydraulic properties (K, van Genuchten curves)  

  - Drainage layout, rainfall/evaporation data  

  - Logger data for calibration  

---

**2. Surface Flow & Barrier Routing Models**  
Examples: **HEC-RAS 2D**, **TELEMAC-2D**  

- Simulate: how roads, tracks, or berms act as **barriers**, causing ponding or fragmentation between pools  

- Inputs:  
  - Sub-metre DEM  

  - Roughness maps (e.g. open water vs. Sphagnum mats)  

  - Rainfall hyetographs  

  - Water-level data from pool loggers  

---

**3. Catchment-Scale Conceptual Screening Models**  
Examples: **TOPMODEL**, **HBV**, **GR4J** (with peat-specific parameters)  

- Simulate: broader **seasonal drawdown risks**, “what-if” scenarios of cumulative impact  

- Inputs:  
  - Rainfall and evapotranspiration time series  

  - Simplified soil and land cover types  

  - Outflow measurements or dipwell data  

---

**4. Peatland-Specific Eco-Hydrological Models**  
Example: **DigiBog**  

- Simulate: long-term interaction between **peat growth** and **hydrology**, particularly pool–ridge feedback  

- Inputs:  
  - Microtopography  

  - Peat decomposition and productivity parameters  

  - Historic water-table records  

- Notes: DigiBog also includes a standalone hydrology module (*DigiBog_Hydro*)  

More info: [https://www.peatmothership.org/digibog](https://www.peatmothership.org/digibog)

---

**5. Graph-Based & Cellular Automata Models (from LiDAR)**  

- Simulate: how **microtopography** and barriers affect **connectivity** between pools  

- Can model thresholds for hydrological fragmentation and loss of function  

- Inputs:  
  - High-resolution DEM  

  - Seasonal pool extents  

  - Mapped pool network  

---

**6. Water Quality & Export Models**  
Examples: **SWAT+**, **HYPE** (peat-parameterised)  

- Simulate: how construction corridors affect **DOC (dissolved organic carbon)** or sediment exports  

- Inputs:  
  - Soil carbon maps, surface runoff patterns  

  - Event-based water sampling of DOC and turbidity  

---

#### Explanation of Key Terms

- **van Genuchten curves**: Describe how water is retained in soil/peat at different tensions — needed for accurate modelling of flow through porous media  

- **GW–SW exchange**: The bidirectional flow between groundwater and surface water (like pools)  

- **Hyetograph**: Graph of rainfall intensity over time  

- **Hydroperiod**: Duration and frequency of pool inundation  

- **Acrotelm/Catotelm**: The upper active and lower anoxic peat layers in bogs

---

#### Final Aim

The aim of this group is not to develop a working model immediately, but to outline:

- A **recommendation** for model type and structure  

- A minimum data standard for ecological assessments  

- Possible avenues for future development (student projects, grant proposals, open-source collaboration)