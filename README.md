# Changelog

**Caution! These files are only usable with _Euroscope_ and are no longer compatible with VRC!**

**For VRC use the old 0904 version.**

## v. 1209

### Global changes
* GEO area is now divided into sub-areas that can be displayed or hidden individually (Display Settings > GEO).
  Previously all GEO could only be displayed or hidden at once. The new GEO areas are as follows: LQSA Ground, LQSA
  Major Stands, LQSA Minor Stands, LQSA MSA Sectors, LQBK Ground, LQMO Ground
* Renamed ARTCC and ARTCC High Areas to more human-readable names (Display options > ARTCC boundary, ARTCC high
  boundary to enable). The FIRs affected and their new names are: LDZO FIR, LYBA FIR, LQSB FIR, LQSB TMAs,
  PRISHTINA FIR/UIR
* Renamed ARTCC Low Areas to more human-readable names (Display options > ARTCC low boundary to enable). The zones
  affected and their new names are: LQSA Control Zone, LQMO Control Zone, LQBK Control Zone, LQBK TCA

### LQSA changes
* LQSA_GND position now has its own dedicated mini "sector" in ES. This allows the position to be associated with LQSA
  airport and the airport will be marked as active and latest metar loaded upon logging as GND. Just like TWR and APP.
  You can see how it looks on [this picture](http://imgur.com/6tk2B).
* The track of the ILS Y 12 approach and Timid holding is no longer defined as GEO. It is now a STAR and can be
  optionally displayed or hidden (Display Options > Stars). Also you can choose the line style, color and thickness
  via the Symbology options. It could look for example [like this](http://imgur.com/9HZ8c).
* LQSA MSA values are no longer defined as fixes, they are now freetext (Display Options > Freetext) and can be
  enabled/disabled as a group or individually
* Added the second hold short line on A for LQSA
* Added stand 11D
* Stand markings for all major stands or minor stands can be optionally displayed or hidden independent on the ground
  layout (Display Options > GEO > LQSA Minor Stands, LQSA Major Stands)
* The taxiway letters are now displayed ON the taxiways and not next to them
* minor adjustements to LQSA station data


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
  **Required vis ranges** to match the preset centers: APP: 50 nm; TWR: 35 nm; GND: 10 nm. Approximate visibility radius
  around LQSA with these settings is: GND: 18nm, TWR: 60nm, APP: 90nm. Vis centers can always be overriden in ES.
* adjusted accurate sq ranges for all BiH airports
* when logging on any LQSA station and selecting the airport as active, LQSA Metar will automatically be loaded
  in your list of metars (no need to press F2 and add it manually in the start of the session)
* changed colour of LQSA radar minimums areas to teal to avoid overlapping with the extened centerline and vectoring grid
* removed waypoints/navaids: SAR VOR
* added waypoints/navaids: OMA VOR
* removed all airports and runways outside BiH
* removed procedures: STAR:LQSA:12:VINCE + all procedures outside BiH
* adjusted magnetic variation and lat/long scaling grid of the entire sector to match current values
* removed from ESE file: all CTR/TMA info which is not relevant for BiH traffic: Budapest, Vienna, Ljubljana,
  Milano, Brindisi, Pula, Rijeka, Zadar, Brac (this only affects tracking, handoffs and coordination)

#### LQSA Ground Layout changes:
* completely reworked parking positions: all major and minor stands are drawn on their exact positions, matching
  latest scenery by Dragomir Andonovic. Major stands are yellow, minor stands are red.
* added parking position designators for all major and minor  that can be shown or hidden individually
  (Display Options > Freetext)
* moved taxiways B and C to their proper position and adjusted their shapes. They now match exactly
  latest scenery by Dragomir Andonovic.
* apron redrawn and extended to the NW to match the RL layout and the latest scenery
* added hold short lines for A, B, and C, matching latest scenery
* added taxiway designators, that can be displayed through the Display Options > Freetext dialog
* added rwy designators and TORA values (Display Options > Freetext)

## Installation

### Upgrading from version 1208

**Replace your local `sct` and `ese` files with the files from this package:**

* LQSB.sct
* LQSB.ese

*Go through your Euroscope > Display Options to enable/disable new features*

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

**Remember:** You can always adjust which elements you wan to see and also colours and sizes from your Symbology Settings
in ES. Some features are useful for newbie ATCs and not needed for advanced controllers, and sometimes it's the opposite.
Choose according to your taste and needs.

__With Euroscope you DON'T NEED pof files and a new rwy file will be automatically generated based on the new sector file.__

_**NOTE:** Because of the new sector file, you'll need to reconfigure your ES display
options and re-create your Radar display views (asr files). This is a one-time only operation
when upgrading from v. 0904 and you won't need to do it again for later versions._
