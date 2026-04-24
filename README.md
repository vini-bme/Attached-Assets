# FlexiMap Suite

## Project Overview
FlexiMap Suite is a computational bioinformatics platform developed for the 2026 Google Solution Challenge. The tool is designed to assist researchers in drug discovery by visualizing protein flexibility and identifying allosteric mapping pathways. By utilizing Elastic Network Models (ENM), the suite highlights conserved hinges and dynamic residues that are critical for therapeutic targeting.

## Key Features
* **Allosteric Site Identification:** Automated detection of non-orthosteric binding sites through per-residue dynamic analysis.
* **Structural Comparative Analysis:** Normalized overlay charts for comparing flexibility profiles across multiple protein structures.
* **Interactive 3D Visualization:** High-fidelity molecular rendering for real-time structural inspection.
* **AI-Driven Interpretation:** Automated insights into the functional implications of identified protein hinges.

## Technical Stack
* **Language:** Python 3.10+, TypeScript 5.0+
* **Backend:** Flask, ProDy, Biopython, NumPy, SciPy
* **Frontend:** React, Vite, Tailwind CSS
* **Environment:** Replit Nix-based infrastructure

## Installation and Local Development
To run the project locally, ensure you have Python and Node.js installed.

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/vini-bme/Attached-Assets.git](https://github.com/vini-bme/Attached-Assets.git)
   cd Attached-Assets

2. **Install Backend Dependencies:**
   ```bash
   pip install -r requirements.txt

4. **Install Frontend Dependencies:**
   ```bash
   npm install

6. **Launch the Application:**
   ```bash
   python main.py

## Repository Structure
* **/src:** Frontend React components and TypeScript logic.

* **/public:** Static assets and structural data files.

* **app.py / main.py:** Flask backend entry points.

* **requirements.txt:** Python dependency manifest.

* **replit.nix:** System-level configuration for deployment.

## Submission Information
* **Event:** Google Solution Challenge 2026

* **Project Status:** MVP (Minimum Viable Product)

* **Access:** Public Repository
