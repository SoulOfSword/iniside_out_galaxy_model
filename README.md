# Inside-out Galaxy Evolution Model for Star-Forming Galaxies

This thesis explores the baryonic specific angular momentum–mass–gas fraction $(j_{\mathrm{bar}} - M_{\mathrm{bar}} - f_{\mathrm{gas}})$ relation in star-forming (disk) galaxies and investigates how different star formation laws (including the classical Kennicutt–Schmidt law and a version of the Boissier law) affect it.

A semi-analytical model is developed that:
1. **Assumes inside-out growth** — gas accretes at larger radii over time.
2. **Implements various star formation laws** fitted to observational data, capturing both high-density (inner) and low-density (outer) regions of galactic disks.
3. **Keeps rotation velocity fixed in time**, to avoid artificially adding angular momentum, while allowing it to vary with radius according to a simple exponential function.

**Key results** show that:
- The *inside-out accretion* assumption is crucial for reproducing the observed $(j_{\mathrm{bar}} - M_{\mathrm{bar}} - f_{\mathrm{gas}})$ relation.
- Different star formation laws yield noticeable differences in **radial profiles** of gas and stars but do **not** dramatically change the overall $(j_{\mathrm{bar}} - M_{\mathrm{bar}} - f_{\mathrm{gas}})$ relation.
- Revised laws provide a better match to observed surface densities in galaxy outskirts compared to the classical Kennicutt–Schmidt law.

You can read the this is [here](https://fse.studenttheses.ub.rug.nl/33339/).

---

**Code Implementation**

The code in this repository provides a Python-based implementation of the above galaxy evolution model. It numerically solves the relevant differential equations for gas and stellar surface densities under different star formation laws, using a Runge-Kutta approach. You can configure parameters such as:
- **Accretion history** (timescale or frequency, total baryonic mass).
- **Star formation law** (Kennicutt–Schmidt (original or revised) or Boissier).
- **Rotation curve** (flat or radially varying).

Results include radial profiles of gas, stars, and star formation rates, as well as global properties like the baryonic mass, gas fraction, and specific angular momentum. These can be compared to observations for validation.

---

**Data Sources**

- **Star Formation Laws**: We fit the Kennicutt–Schmidt and Boissier laws using the dataset compiled by [Bacchini et al. (2020)](https://ui.adsabs.harvard.edu/abs/2020A%26A...641A..70B/abstract), which includes also low density regions of galaxies. Dwarf galaxy HI data and rotation velocities are taken from [Iorio et al. (2017)](https://ui.adsabs.harvard.edu/abs/2017MNRAS.466.4159I/abstract) (LITTLE THINGS sample; [Hunter et al. (2012)](https://ui.adsabs.harvard.edu/abs/2012AJ....144..134H/abstract)), while star formation rates come from FUV photometry ([Zhang et al. (2012)](https://ui.adsabs.harvard.edu/abs/2012MNRAS.424..665Z/abstract)) calibrated via [McQuinn et al. (2015)](https://ui.adsabs.harvard.edu/abs/2015ApJ...812..158M/abstract). For spiral galaxies, HI and SFR densities are from [Leroy et al. (2008)](https://ui.adsabs.harvard.edu/abs/2008AJ....136.2782L/abstract), H2 from [Frank et al. (2016)](https://ui.adsabs.harvard.edu/abs/2016MNRAS.457.1722F/abstract) with a CO conversion factor ([Sandstrom et al. (2013)](https://ui.adsabs.harvard.edu/abs/2013ApJ...777....5S/abstract)), and rotation velocities from [Bacchini et al. (2019, 2020)](https://ui.adsabs.harvard.edu/abs/2019A%26A...622A..64B/abstract).

- **Rotation Curves**: To model radially varying rotation speeds, we use the [SPARC catalog](https://ui.adsabs.harvard.edu/abs/2016AJ....152..157L/abstract) ([Lelli et al. (2016)](https://ui.adsabs.harvard.edu/abs/2016AJ....152..157L/abstract)) to fit an exponential rotation curve and link it to the asymptotic flat velocity.

- **Scaling Relations**: We compare our results for $j_{\mathrm{bar}}, M_{\mathrm{bar}}, f_{\mathrm{gas}}$ against the observational relation reported by [Mancera Piña et al. (2021b)](https://ui.adsabs.harvard.edu/abs/2021Natur.594..485M/abstract). We also adopt the Baryonic Tully–Fisher relation from [McGaugh (2012)](https://ui.adsabs.harvard.edu/abs/2012AJ....143...40M/abstract) to fix the final rotation velocity of each galaxy.
