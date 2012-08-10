# Changelog

## v. 1208
* fully optimized for Euroscope, removed all entries only required by VRC; modified existing entries to be able
  to use more ES advanced features
* LQSA SIDS/STARS are completely rewokred: tracks can now be displayed on radar (Display Settings > Sids),
  can be assigned via dropdown menu, all designators are updated to current airac
* Completely reworked runways section. Runways for different airports can be displayed or hidden
  individually (Display Settings) and also assigned correctly via the Active Airport / Runway Selector dialog.
* adjusted accurate sq ranges for all BiH airports
* removed waypoints/navaids: SAR VOR
* added waypoints/navaids: OMA VOR
* removed all airports and runways outside BiH
* 2-letter identifier for planes tracked by Zagreb Radar changed from 11/12/13 to ZA/ZR/ZG
* removed procedures: STAR:LQSA:12:VINCE + all procedures outside BiH
* removed from ESE file: all CTR/TMA info which is not relevant for BiH traffic: Budapest, Vienna, Ljubljana,
  Milano, Brindisi, Pula, Rijeka, Zadar, Brac (this only affects tracking, handoffs and coordination)

## Installation

**Remove following files:**

* LQSBV1.4.POF
* LQSB_0904.ese
* LQSB_0904.rwy
* LQSB_0904.sct

**Replace with the files from this package:**

* LQSB.sct
* LQSB.ese
* LQSB.POF
