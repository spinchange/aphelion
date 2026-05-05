---
title: Space Debris
author: claude-sonnet-4-6
date: 2026-05-05
status: active
aliases: [space debris, orbital debris, space junk, MMOD, Kessler syndrome, ODPO]
type: permanent
provenance:
  source_page_ids:
    - 4132fd45-43ba-48b3-9779-0defd289fee5
    - 08cd9bf0-dafd-4c73-be0d-1d8f61944a24
    - 9a5eba47-b4e5-49b8-be61-df845a0cdb24
    - a1feb4ba-def0-4e61-b4bf-668199a6812b
    - 53b00920-8258-42c1-a9aa-4fb1fc612dac
    - c4ba1e37-85a1-4623-a753-b9ff13f01297
    - 273b914d-7825-43a9-9f4c-eec17e92ad5c
    - aa28604e-63e9-4c98-a014-8be62de808a5
  sources:
    - https://en.wikipedia.org/wiki/Space_debris
    - https://orbitaldebris.jsc.nasa.gov/
  retrieved_at: 2026-05-05
  acting_agent: claude-chronicler
---

# Space Debris

Defunct human-made objects in Earth orbit that no longer serve a useful function: derelict spacecraft, abandoned launch stages, mission-related debris, and fragmentation debris from breakups and collisions. A growing hazard to operational spacecraft and the long-term usability of orbital regimes. Referenced in [[geospace]] as a major threat to near-Earth space activity; created in part by the ASAT weapons permitted under the [[outer-space-treaty]].

## Population (NASA ODPO Estimates)

The **NASA Orbital Debris Program Office (ODPO)** is the authoritative source for debris population data:

| Size | Estimated count | Status |
|---|---|---|
| ≥10 cm | ~40,000+ | Tracked by Space Surveillance Networks |
| Marble-sized (~1 cm) | ~500,000 | Predicted, not individually tracked |
| ≤1 mm | >100,000,000 | Estimated |

Objects large enough to be tracked are catalogued by the U.S. Combined Space Operations Center's Space Surveillance Network. Below ~10 cm objects are too small to track reliably but large enough to be mission-ending on impact. Even the smallest objects are dangerous at orbital velocities (~10 km/s in LEO).

## Measurement Methods (ODPO)

The ODPO measures the debris environment through multiple complementary methods:

- **Ground-based radar** — Haystack X-Band Radar and others in the U.S. Space Surveillance Network
- **Optical telescopes** — ground-based tracking of objects in higher orbits
- **Space-based sensors** — in-situ measurements from orbit
- **Returned spacecraft surfaces** — direct physical analysis of impact craters on Solar Max, the Long Duration Exposure Facility (LDEF), Hubble Space Telescope, and Space Shuttle surfaces
- **DebriSat** — ground-based lab experiments to characterize fragmentation

Data feeds directly into the ODPO's environment models.

## Modeling Tools (ODPO)

**ORDEM 3.2** (Orbital Debris Engineering Model) — Engineering model for debris impact risk assessments on spacecraft and satellites, including the ISS. Covers LEO to GEO altitudes, object sizes from 10 µm to 1 m, for 2016–2050. Updated to include fragments from the Cosmos 1408 ASAT test (Russia, 15 November 2021). Available as a desktop application and a cloud-based web app.

**LEGEND** (LEO-to-GEO Environment Debris model) — 3D evolutionary model for long-term debris environment projection, covering 200–50,000 km altitude. Runs 100+ Monte Carlo simulations over 200-year projection periods to account for uncertainties in future launch traffic, solar activity, and collision events.

**DAS** (Debris Assessment Software) and **ORSAT** (Object Reentry Survival Analysis Tool) — Compute reentry survivability and predict risk to humans on the ground from reentering rocket bodies and spacecraft.

## Kessler Syndrome

Proposed by NASA scientist Donald J. Kessler in 1978: if debris density in low Earth orbit (LEO) exceeds a critical threshold, collisions generate more debris, increasing collision probability in a runaway cascade. Certain orbital bands could be rendered economically unusable for many generations.

The **2009 Iridium 33 / Kosmos 2251 collision** — the first major satellite collision — destroyed both satellites at ~11.7 km/s and produced thousands of fragments. Two LEO bands (900–1,000 km and 1,500 km) are already considered past critical density by the US National Academy of Sciences.

Notable ASAT-generated debris events:
- **2007 Chinese ASAT test** — largest single debris-generating event in history
- **2021 Cosmos 1408 ASAT test** (Russia) — generated fragments now tracked in ORDEM 3.2

## Sources and Origins

- Fragmentation from satellite and rocket body breakups (battery explosions, pressurized tank failures)
- ASAT weapon tests
- Satellite-on-satellite collisions
- Surface erosion: paint flakes, solid rocket exhaust particles
- Frozen coolant from Soviet nuclear-powered RORSAT satellites

## Protection Research

The ODPO's **Hypervelocity Impact Technology Facility (HITF)** at Johnson Space Center conducts hypervelocity impact tests to assess debris risk and develop improved shielding materials. Research output informs Whipple shield design standards and spacecraft operations procedures.

## Mitigation

ODPO developed the first NASA orbital debris mitigation requirements in 1995. Current guidelines (not binding law) recommend deorbiting LEO objects within 25 years of end of mission. Atmospheric drag is the primary natural removal mechanism below ~600 km; above that, debris persists for centuries.

The debris problem is a **negative externality** — operators do not bear the full cost of debris they create, which makes international coordination structurally difficult despite broad scientific consensus on the risk.
