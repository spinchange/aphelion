---
title: Dead Reckoning
author: claude-sonnet-4-6
date: 2026-05-17
status: active
aliases: [dead reckoning navigation, DR navigation, ded reckoning, position estimation]
type: permanent
---

# Dead Reckoning

Dead reckoning is a method of navigation in which a current position is estimated by starting from a known position and advancing it using known or estimated speed, direction, and elapsed time — without reference to external landmarks or celestial observations. It is the backbone of all navigation in conditions where external references are unavailable, and it remained the primary navigation method for ocean sailing from antiquity through the late 18th century.

## The Method

Starting from a *fix* — a position known with confidence, established by celestial observation, landmark, or chart — the navigator applies:

1. **Course** — the direction of travel (compass bearing)
2. **Speed** — estimated from log-line readings, engine rpm, or wind judgment
3. **Time** — elapsed since the last fix

Multiplying speed by time gives distance run. Applying the course gives the direction. The result is the estimated position — the *DR position*. Each hour the navigator updates the DR position: advance the plot by the distance run on the heading steered.

Errors compound. A small error in speed estimate, a slight current unaccounted for, a compass deviation — each advances the DR position slightly wrong, and over days of ocean crossing the errors accumulate. A ship crossing the Atlantic by dead reckoning alone might arrive with a longitude error of hundreds of miles. This is why [[celestial-navigation]] — which provides periodic accurate fixes — was so critical: it reset the accumulated DR error.

## Historical Centrality

Dead reckoning was the default method for the entire Age of Exploration. Columbus, Magellan, and every other ocean navigator of the 15th and 16th centuries crossed unknown waters primarily by dead reckoning — keeping careful track of course and distance, estimating their longitude by accumulated run from a known departure point.

The errors were accepted as the cost of ocean navigation. The [[longitude-problem]] — how to know your east-west position accurately — was precisely the problem of fixing the accumulated longitude error in the DR track. John Harrison's chronometer (1760s) solved the longitude problem by providing accurate time at sea, which enabled celestial observation to give precise longitude, which enabled accurate fixes to reset the DR accumulation.

Before the chronometer, skilled navigators used dead reckoning supplemented by latitude observations (measurable from sun or star altitude) and educated guesses about longitude. The latitude was reliable; the longitude was estimated. This is why early charts show reasonable accuracy in the north-south dimension and distorted east-west dimensions.

## Error Sources

The main error sources in dead reckoning:
- **Current** — ocean currents carry the vessel off course silently; the compass heading is correct but the actual track deviates
- **Leeway** — wind pushes sailing ships sideways; the bow points one way, the actual path diverges
- **Speed error** — log-line measurements are approximate; tidal cycles affect apparent progress
- **Compass error** — variation (the difference between magnetic and true north, which varies by location) and deviation (distortion caused by the ship's own magnetic field)

Skilled navigators developed intuitions for these corrections. Dead reckoning was not guessing — it was systematic estimation with understood error sources managed by experience.

## Modern Dead Reckoning

Dead reckoning never became obsolete — it became more precise. Modern applications:

- **Inertial navigation systems (INS)** — aircraft and missiles use accelerometers and gyroscopes to continuously integrate acceleration into velocity and velocity into position; this is dead reckoning at high precision, used when GPS is unavailable or jammed
- **Autonomous vehicles** — wheel odometry and IMU data maintain position estimates between GPS fixes
- **Submarine navigation** — submerged submarines navigate primarily by inertial dead reckoning; GPS and celestial observations are impossible
- **Spacecraft** — interplanetary probes navigate by dead reckoning from mission-calculated trajectory models, with periodic fixes from celestial observations or ground tracking

The principle is unchanged: start from a known position, integrate movement. The difference is that modern sensors accumulate error far more slowly — INS systems on aircraft drift by 1-2 nautical miles per hour rather than the dozens of miles per day achievable by 15th-century ocean navigation.

## Etymology

The origin of "dead" in "dead reckoning" is debated. The most likely derivation is from "deduced reckoning" — abbreviated to "ded. reckoning" and then misread as "dead." Alternative theories include the nautical usage of "dead" to mean "directly" (as in "dead ahead") or a reference to the reckoning being done from a dead (stationary, known) position.

## See Also

- [[celestial-navigation]] — the periodic fix source that resets dead reckoning error
- [[longitude-problem]] — the historical failure of dead reckoning in the east-west dimension
- [[compass]] — the direction-giving instrument at the heart of DR navigation
- [[sextant]] — the instrument used to take celestial fixes that correct DR drift
- [[polynesian-navigation]] — an alternative tradition that minimised dead reckoning by reading environmental signals directly
