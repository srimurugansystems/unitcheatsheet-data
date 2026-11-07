# unitcheatsheet.com open data

Unit definitions, conversion factors and engineering tables behind [unitcheatsheet.com](https://unitcheatsheet.com/), generated from the same data and formulas the site uses.

**Licence:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Attribution: "unitcheatsheet.com open data (https://unitcheatsheet.com/data.html), CC BY 4.0".

| File | What it holds | Rows | Source |
|---|---|---|---|
| `units.csv` | Every unit with a fixed factor: its value in the base unit of its category, whether the definition is exact, and the official source. The temperature scales and fuel-economy units are defined by formulas, given in units.json. | 183 | NIST SP 811, NIST Handbook 44, BIPM SI Brochure, NIST binary prefixes, UK Weights and Measures Act 1985 |
| `conversions.csv` | One row per converter page: multiply the 'from' value by the factor to get the 'to' value. Temperature pairs use the formulas in units.json. | 109 | Derived with exact arithmetic from units.csv |
| `conversion-values.csv` | The values that have their own page on the site (for example 37 °C in °F), converted with the factors above. | 146 | Computed from conversions.csv |
| `awg.csv` | Diameter and cross-section of American Wire Gauge sizes 4/0 to 40, from the defining formula d = 0.005 in × 92^((36 − n)/39) (ASTM B258). Ampacity is not included. | 44 | Computed from the AWG formula (ASTM B258) |
| `npt-threads.csv` | American Standard taper pipe threads (NPT): threads per inch, outside diameter, pitch diameters E0 and E1, hand-tight engagement L1 and effective thread length L2, in inches. | 14 | NBS Handbook H28 (1957), Part II, Table VII.2 (US government publication, public domain); checked 7 November 2026 |
| `water-density.csv` | Density of air-free pure water at 101.325 kPa and the weight of one US gallon, from the CIPM-recommended formula. | 41 | CIPM formula, Tanaka et al., Metrologia 38 (2001) 301–309, as published by NIST |
| `boiling-point-altitude.csv` | Standard-atmosphere pressure and the boiling point of pure water from sea level to 8,849 m. | 37 | IAPWS R7-97(2012) Region 4 equation; U.S. Standard Atmosphere, 1976 |
| `wind-chill.csv` | Wind chill temperature in °F for air temperatures from 40 °F to −45 °F and wind speeds from 5 to 60 mph. | 216 | National Weather Service wind chill formula (2001) |
| `tasks.json` | Common engineering jobs as ordered steps across the site's pages. | 23 | unitcheatsheet.com |
| `verification.json` | What was checked against which official source, when, for which pages. | 16 | unitcheatsheet.com |

Also: `units.json` (units with sources, plus the temperature and fuel-economy formulas), `datapackage.json` (Frictionless Data descriptor), `CITATION.cff`.

**Not included:** tables taken from copyrighted or paid standards and handbooks (NEC ampacity, ISO tolerances, ANSI drill sizes, SAE O-rings, Machinery's Handbook tap drills, the CDA Copper Tube Handbook). They are shown on the site with their sources, but no licence to them is offered here.

**Accuracy:** factors are checked against NIST and BIPM with exact arithmetic; see `verification.json` for what was checked and when. Report an error to contactus@unitcheatsheet.com; fixes are listed at https://unitcheatsheet.com/changelog.html.
