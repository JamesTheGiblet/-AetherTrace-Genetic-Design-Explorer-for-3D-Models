🧬 AetherTrace – Genetic Design Explorer for 3D Models
Evolve Meshes, Shape Creativity

AetherTrace is a genetic algorithm-driven tool for evolving 3D mesh designs. Users guide evolution through manual selection or functional fitness goals (symmetry, curvature, volume, etc.). Available as a Blender add-on or standalone PyQt6/Gradio app, AetherTrace transforms procedural design into an organic, adaptive process.
🔥 Key Features

    ✅ Genetic Evolution Engine – Mutate, crossover, and optimize 3D meshes dynamically

    ✅ Fitness-Based Selection – Auto or manual scoring for optimized form exploration

    ✅ Blender & Standalone UI – Use within Blender or as an independent PyQt6/Gradio tool

    ✅ AI Aesthetic Predictor (optional) – ML-driven beauty scoring for evolved shapes

    ✅ Style Guidance – Train models toward specific forms or design traits

🚀 How It Works

AetherTrace evolves 3D designs using genetic algorithms, iterating toward optimal forms through mutation and selection.
Genome Representation

Each mesh individual is stored as a modifiable genome:

{
  "base_mesh": "sphere",          # Reference shape
  "modifiers": {
     "subdivision": 2,
     "noise_scale": 0.3,
     "extrusion_variance": 0.5,
     ...
  },
  "fitness": 0.82
}

Evolution Flow

    Generate an initial population of N meshes

    Apply modifiers to evolve shapes

    Score each shape based on user-selected fitness criteria

    Select top K meshes as parents

    Perform crossover + mutation for new generation

    Repeat until user stops or optimal form emerges

Fitness Scoring Options

    🔹 Symmetry detection (mirrored deviation analysis)

    🔹 Surface area / volume ratio (compactness metric)

    🔹 Curvature continuity (Laplacian smoothness)

    🔹 Manual selection – click favorite models

    🔹 AI Beauty Score (optional, ML-based aesthetic ranking)

🏗️ Project Structure

aethertrace/
│
├── core/
│   ├── genetic_engine.py         # Handles selection, mutation, crossover
│   ├── fitness_functions.py      # Curvature, volume, symmetry scoring
│   ├── mesh_io.py                # Load/save meshes, .obj/.blend export
│   ├── mesh_mutation.py          # Functions for deforming meshes
│   ├── utils.py                  # Common helpers
│
├── gui/
│   ├── qt_ui.py                  # PyQt6 GUI (optional)
│   ├── blender_panel.py          # Blender add-on version (optional)
│
├── ai/
│   ├── aesthetic_predictor.py    # ML model to evaluate mesh beauty (optional)
│   └── latent_embedding.py       # Embeds meshes/images for guidance
│
├── data/
│   ├── presets/                  # Sample starting meshes
│   └── logs/                     # Saved generations
│
├── tests/
│   └── test_genetics.py          # Unit tests
│
├── main.py                       # Entry point
└── README.md

🖥️ UI & Workflow

AetherTrace offers two primary user interfaces:
Option A: Blender Add-On

    Add-on panel to configure genetic parameters

    View & select evolved meshes directly in Blender

    Thumbnail previews of generations

Option B: Standalone PyQt6/Gradio App

    Load, mutate & evolve mesh files (.OBJ/.STL)

    Real-time visual feedback for evolution steps

    AI-based mesh stylization (optional)

🔮 Future Enhancements

    ✨ Multi-object breeding (combine two base meshes)

    ✨ Behavioral trait tagging (“aggressive”, “smooth”, “mechanical”)

    ✨ Export pipeline for Unity/Unreal asset generation

    ✨ 3D printing compatibility check

🛠️ Installation

Clone the repo and set up dependencies:

git clone [https://github.com/JamesTheGiblet/AetherTrace.git](https://github.com/JamesTheGiblet/AetherTrace.git)
cd AetherTrace
pip install -r requirements.txt

Launch standalone:

python main.py

For Blender integration:

    Open Blender

    Install as an add-on from the GUI

🌎 Community & Collaboration

Join development discussions and contribute ideas! Pull requests are welcome. 🚀
