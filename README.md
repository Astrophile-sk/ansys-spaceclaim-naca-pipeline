# ANSYS SpaceClaim Automated NACA Airfoil & CFD Domain Generator

An automated Python script for **ANSYS SpaceClaim** that generates 2D NACA 4-digit airfoil geometries, builds a surrounding 2D fluid domain, and assigns boundary **Named Selections** (inlet, outlet, walls, irfoil) for ANSYS Fluent and Fluent Meshing.

---

## Features (v1.0.0)

* **Cosine Clustering:** Uses cosine point distribution along the chord for high resolution at leading and trailing edges.
* **Automated Surface Creation:** Generates planar domain surfaces and extracts the inner airfoil cutout automatically.
* **Vertex-Inset Bounding Box Selections:** Uses dynamic bounding boxes with margin offsets to assign inlet, outlet, walls, and irfoil boundary groups without corner edge collision issues.
* **Macro-Free Execution:** Replaces transient GUI selection IDs (Edge1, Face2) with spatial filters for 100% reproducible execution across fresh SpaceClaim sessions.

---

## How to Run in SpaceClaim

1. Launch **ANSYS SpaceClaim**.
2. Open the Scripting tab (Design -> Scripting or File -> New Script).
3. Copy and paste the contents of [
aca_airfoil_generator.py](./naca_airfoil_generator.py).
4. Click **Run** (F5).

---

## Version Roadmap

- [x] **v1.0.0:** Baseline NACA 4412 SpaceClaim automation & robust CFD domain named selections.
- [ ] **v1.1.0:** Parametric chord scaling (c) & symmetric profile support (NACA 00xx series).
- [ ] **v1.2.0:** Angle of Attack ($\alpha$) rotation matrix around quarter-chord (.25c$).
- [ ] **v2.0.0:** Command-line headless batch execution for polar sweeps ($\alpha = -4^\circ \text{ to } 16^\circ$).

---

## License

Distributed under the MIT License. See LICENSE for details.
