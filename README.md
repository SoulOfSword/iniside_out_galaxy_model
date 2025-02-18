# Inside-out Galaxy Evolution Model for Star-Forming Galaxies

This thesis explores the baryonic specific angular momentum–mass–gas fraction $(j_{\mathrm{bar}} - M_{\mathrm{bar}} - f_{\mathrm{gas}})$ relation in spiral galaxies and investigates how different star formation laws (including the classical Kennicutt–Schmidt law and a version of the Boissier law) affect it.

A semi-analytical model is developed that:
1. **Assumes inside-out growth** — gas accretes at larger radii over time.
2. **Implements various star formation laws** fitted to observational data, capturing both high-density (inner) and low-density (outer) regions of galactic disks.
3. **Keeps rotation velocity fixed in time**, to avoid artificially adding angular momentum, while allowing it to vary with radius according to a simple exponential function.

**Key results** show that:
- The *inside-out accretion* assumption is crucial for reproducing the observed $(j_{\mathrm{bar}} - M_{\mathrm{bar}} - f_{\mathrm{gas}})$ relation.
- Different star formation laws yield noticeable differences in **radial profiles** of gas and stars but do **not** dramatically change the overall $(j_{\mathrm{bar}} - M_{\mathrm{bar}} - f_{\mathrm{gas}})$ relation.
- Revised laws provide a better match to observed surface densities in galaxy outskirts compared to the classical Kennicutt–Schmidt law.

---

**Code Implementation**

The code in this repository provides a Python-based implementation of the above galaxy evolution model. It numerically solves the relevant differential equations for gas and stellar surface densities under different star formation laws, using a Runge-Kutta approach. You can configure parameters such as:
- **Accretion history** (timescale, total baryonic mass).
- **Star formation law** (Kennicutt–Schmidt or Boissier).
- **Rotation curve** (flat or radially varying).

Results include radial profiles of gas, stars, and star formation rates, as well as global properties like the baryonic mass, gas fraction, and specific angular momentum. These can be compared to observations for validation.
