# Changelog

**Caution! These files are only usable with _Euroscope_ and are no longer compatible with VRC!
For VRC use the old 0904 version.**

## v. 1208
* fully optimized for Euroscope, removed all entries only required by VRC; modified existing entries to be able
  to use more ES advanced features.
* LQSA SIDS/STARS are completely rewokred: tracks can now be displayed on radar (Display Settings > Sids),
  can be assigned via dropdown menu, all designators are updated to current airac. Interim waypoints in
  SIDs can now be displayed along the route of tagged a/c and used for time prediction, coordination and directs.
* Completely reworked runways section. Runways for different airports can be displayed or hidden
  individually (Display Settings) and also assigned correctly via the Active Airport / Runway Selector dialog.
* Reworked positions information for all LQSA stations and Zagreb Radar. More detailed info will be visible in the
  tags of the tracked aircraft. Improved identifiers.
* 4 visibility centers are now associated and automatically activated upon login for all LQSA positions (APP, TWR, GND).
  Required vis ranges to match the preset centers: APP: 50 nm; TWR: 35 nm; GND: 10 nm. Vis centers can always be
  overriden in ES.
* adjusted accurate sq ranges for all BiH airports
* removed waypoints/navaids: SAR VOR
* added waypoints/navaids: OMA VOR
* removed all airports and runways outside BiH
* removed procedures: STAR:LQSA:12:VINCE + all procedures outside BiH
* removed from ESE file: all CTR/TMA info which is not relevant for BiH traffic: Budapest, Vienna, Ljubljana,
  Milano, Brindisi, Pula, Rijeka, Zadar, Brac (this only affects tracking, handoffs and coordination)

## Installation

### Upgrading from version 0904

**Remove the following files:**

* LQSBV1.4.POF
* LQSB_0904.ese
* LQSB_0904.rwy
* LQSB_0904.sct

**Replace with the files from this package:**

* LQSB.sct
* LQSB.ese

Now you can open the new LQSB sector file in your Euroscope.

__ With Euroscope you DON'T NEED rwy and pof files __

_**NOTE:** Because of the new sector file, you'll need to reconfigure your ES display
options and re-create your Radar display views (asr files). This is a one-time only operation
when upgrading from v. 0904 and you won't need to do it again for later versions._