# FlexiMap Suite

A computational biology web app for protein flexibility analysis and allosteric drug discovery. Built for the **Google Solution Challenge 2026**.

**Live Demo:** https://attached-assets--vini36931052006.replit.app

---

## What it does

Researchers upload a protein structure file (.pdb) and the app computes how flexible each part of the protein is. Flexible regions (called hinges) are the best spots to target with drugs. FlexiMap makes this analysis fast and visual.

---

## Features

### Analytics & Education
- Upload any `.pdb` protein structure file
- Computes Gaussian Network Model (GNM) dynamics using ProDy
- Shows a live **3D flexibility map** — red = highly flexible, blue = rigid
- **Per-residue flexibility chart** showing all hinge peaks
- **Residue fluctuation table** sortable and exportable as CSV
- AI-powered structural insights via Gemini API
- "For Students" section explains the science in simple terms

### Ligand Docking Simulator
- Enter a peptide or ligand sequence
- Simulates a docking event against the highest-flexibility hinge region
- Shows pre-docking vs post-docking comparison
- Outputs: binding affinity (kcal/mol), conformation shift (RMSD), targetability score, stabilized residues
- **Stabilization Map** shows which residues got locked after docking

### Pocket Profiler
- Lists the top 15 most flexible residues ranked by GNM fluctuation
- Shows polarity, charge, and flexibility score for each residue
- Pocket biochemistry fingerprint: composition, hydropathy, charged residues
- AI drug profile generation

### Protein Compare
- Load two protein structures side by side
- Overlaid flexibility profiles (normalized charts)
- Finds **conserved hinge regions** across both proteins with match scores
- Useful for finding drug targets that work across multiple protein variants

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | React, TypeScript, Vite, Tailwind CSS |
| Backend | Python, Flask |
| Biology | ProDy, Biopython, NumPy, SciPy |
| AI | Gemini API |
| Platform | Replit |

---

## How to run locally

```bash
# Clone the repo
git clone https://github.com/vini-bme/Attached-Assets.git
cd Attached-Assets

# Install frontend dependencies
npm install

# Install backend dependencies
pip install -r requirements.txt

# Start the app
python main.py
```

Open http://localhost:5000 in your browser.

---

## Project Status

MVP complete. Submitted to Google Solution Challenge 2026.

* **Access:** Public Repository
