# Project-1-DIY-Wind-Tunnel (view as raw for formatting)
An open-circuit, low-speed wind tunnel built for aerodynamic testing of small-scale models. This project documents the research, design decisions, build plan, and simulation tools for constructing a functional wind tunnel from scratch.
Project Status
Phase                  Status
Research & Planning   ✅ Complete
3D Modeling / Mock-up ✅ Complete
Sourcing Materials    🔲 Not Started
Construction          🔲 Not Started
Testing & Calibration 🔲 Not Started
Simulation Validation 🔲 Not Started

Background — What Are Wind Tunnels Used For?
Wind tunnels simulate airflow around objects, allowing engineers and makers to test shape concepts at a smaller scale before committing to a full design. Key applications include:

Measuring drag and lift on aerodynamic surfaces
Testing designs for aircraft, rockets, cars, and buildings
Improving efficiency and performance during the design process
Validating computer simulations against real-world results


Design Decision: Open vs. Closed Circuit
This build will use an open-circuit design. Here's how the two types compare:
              Open Circuit  Closed Circuit
Cost           ✅ Cheaper      ❌ Expensive

Data           ✅ Better      ❌ Particle contamination buildup
Visualization (smoke clears 
              easily)
              
Complexity    ✅ Simpler to   ❌ More complex
              build
              
Airflow       ⚠️ Affected by  ✅ Predictable, uniform
Quality         room drafts
              
Noise         ⚠️ Loud         ✅ Quieter

Environment   ⚠️ Easily       ✅ Controlled
                contaminated      

Heat          ✅ Vents        ❌ Traps heat
                naturally

Size          ✅ Compact      ❌ Large footprint

Rationale: For a first build focused on flow visualization and learning, open-circuit offers the best balance of cost, simplicity, and accessibility.

🏗️ Build Plan
1. Airflow — Fan Assembly

Fan type: High static pressure fan for consistent airflow
Speed control: ESC (Electronic Speed Controller) for variable, repeatable air speeds
Placement: Fan positioned behind the model (suction configuration) for cleaner upstream airflow

2. Air Conditioning — Filtering Section

Honeycomb mesh: Breaks up large-scale turbulence entering from the inlet
Settling screens: Further filter the airflow to reduce small-scale turbulence before it reaches the test section
Contraction cone: Accelerates and focuses the conditioned air into the test section while maintaining laminar flow

3. Test Section

Built from clear materials to allow full visual inspection of airflow and smoke patterns

Clear acrylic (lightweight, easy to cut)
Polycarbonate (more impact-resistant)


Models will be mounted on a central sting or floor mount

4. Flow Visualization — Smoke Generation

Exploring use of a repurposed vape device as a low-cost smoke generator
Alternative options: incense sticks, theatrical fog machine, or a dedicated smoke wire setup


🖥️ Simulation Tools
Simulations will be used both to inform the build and to validate results after construction.
3D CFD
ToolNotesAVLVortex-lattice method, great for lifting surfacesXFLR5Panel method + viscous flow, good GUI
2D Airfoil Analysis
ToolNotesXfoilIndustry-standard 2D airfoil analysisJavaFoilBrowser-based, great for quick iteration
Propeller / Turbine
ToolNotesQPROPPropeller/motor matching toolXROTORPropeller design and analysis
Full CAD + CFD

SolidWorks (via campus software license) — primary tool for 3D modeling and simulation validation


🖼️ 3D Model / Mock-up

The following render shows the current design mock-up of the wind tunnel assembly.

<!-- Replace the placeholder below with your actual image file once added to the repo -->
Show Image
Fig 1. Open-circuit wind tunnel mock-up — showing inlet, honeycomb section, contraction cone, test section, and fan assembly.

📊 Simulation vs. Real Life

This section will be updated after construction and testing are complete.

Planned comparisons:

Drag coefficient (Cd) from CFD vs. force gauge measurements
Flow visualization (streamlines from simulation vs. smoke patterns in tunnel)
Velocity profile across the test section


📁 Repository Structure
wind-tunnel/
├── README.md               # This file
├── images/
│   └── wind_tunnel_mockup.png   # 3D render / mock-up
├── cad/
│   └── wind_tunnel.SLDPRT  # SolidWorks model files
├── simulations/
│   └── xflr5/              # XFLR5 project files
└── docs/
    └── build_log.md        # Construction notes and progress log
