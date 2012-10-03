# vACCBiH sector/ese files for Euroscope

# Changelog

**Caution! These files are only usable with _Euroscope_ and are no longer compatible with VRC!**

**For VRC use the old 0904 version.**

## v. 1210

### Global changes
* GEO area is now divided into sub-areas that can be displayed or hidden individually (Display Settings > GEO).
  Previously all GEO could only be displayed or hidden at once. The new GEO areas are as follows: LQSA Ground, LQSA
  Major Stands, LQSA Minor Stands, LQSA MSA Sectors, LQBK Ground, LQMO Ground
* Renamed ARTCC and ARTCC High Areas to more human-readable names (Display options > ARTCC boundary, ARTCC high
  boundary to enable). The FIRs affected and their new names are: LDZO FIR, LYBA FIR, LQSB FIR, LQSB TMAs,
  PRISHTINA FIR/UIR
* Renamed ARTCC Low Areas to more human-readable names (Display options > ARTCC low boundary to enable). The zones
  affected and their new names are: LQSA Control Zone, LQMO Control Zone, LQBK Control Zone, LQBK CTA
* Removed navaids: TUZ VOR
* Added navaids: TZU VOR, AS NDB, SAR NDB, GAC NDB, NA NDB, MA NDB, ZV NDB

### LQSA changes
* LQSA_GND position now has its own dedicated mini "sector" in ES. This allows the position to be associated with LQSA
  airport and the airport will be marked as active and latest metar loaded upon logging as GND. Just like TWR and APP.
  You can see how it looks on [this picture](http://imgur.com/6tk2B).
* The track of the ILS Y 12 approach and Timid holding is no longer defined as GEO. It is now a STAR and can be
  optionally displayed or hidden (Display Options > Stars). Also you can choose the line style, color and thickness
  via the Symbology options. It could look for example [like this](http://imgur.com/9HZ8c).
* Added the tracks for all instrument LQSA approaches (ILS Y, NDB Y (same track), ILS Z, NDB Z(same track), Rudar Visual).
  These tracks are defined as STARs and can be hidden or displayed via Display Options > Stars
* LQSA Minimum Radar Altitude (MRA) values are no longer defined as fixes, they are now freetext (Display Options > Freetext)
  and can be enabled/disabled as a group or individually
* Taxiway A redrawn with a correct turn and shape towards 30 threshold to match latest AFCAD
* Added the second hold short line (cat II ILS) on A for LQSA
* Added stand 11D
* Stand markings for all major stands or minor stands can be optionally displayed or hidden independent on the ground
  layout (Display Options > GEO > LQSA Minor Stands, LQSA Major Stands)
* The taxiway letters are now displayed ON the taxiways and not next to them
* Adjusted the shape of the final segment of the KEB 18 DME Arc to now longer deviate from the extended runway centerline
* Changed the preset visiblity centers of LQSA_APP position. Please increase vis range for that position to at least 99nm
  to achieve the desired result. With the new vis settings you'll have vis of more than 150 nm around LQSA, including all
  other BiH airfields
* minor adjustements to LQSA station data

### LQMO changes
* Completely new redrawn LQMO ground to match latest AFCAD and scenery by Dragomir Andonovic. You can see a comparison
  between the old default ground (blue) and the raw version of the new ground (green) [here](http://imgur.com/DKFlE).
  Final version of new LQMO ground can be seen [here](http://imgur.com/tHsPP)
* Added stand positions for Apron 1 and Apron 2, matching the AFCAD
* Added hold short lines on twys A, C, D, E, F, matching latest AFCAD
* added parking position designators for all stands on aprons 1 and 2 that can be shown or hidden individually
  (Display Options > Freetext)
* added taxiway designators, that can be displayed through the Display Options > Freetext dialog
* added rwy designators and TORA values (Display Options > Freetext)
* SIDS are completely rewokred: all SID tracks can now be displayed on radar (Display Settings > Sids),
  can be assigned via dropdown menu, all designators are up-to-date with current airac. Interim waypoints in
  SIDs can now be displayed along the route of tagged a/c and used for time prediction, coordination and directs.
  Screenshot of LQMO TMA with all 1A SIDS displayed: [here](http://imgur.com/Spe0h).
  Another screenshot of LQMO TMA with all 1B SIDS displayed: [click here](http://imgur.com/hbphn).
* Added the tracks for both instrument LQMO approaches (VOR A, NDB A).  These tracks are defined
  as STARs and can be hidden or displayed via Display Options > Stars. Pictue of the VOR app track [here](http://imgur.com/zPEyv)
* 4 visibility centers are now associated and automatically activated upon login for both LQMO positions (APP, TWR).
  **Required minimum vis ranges** to match the preset centers: APP: 99 nm; TWR: 35 nm;
* Default sector ownership logic changed to assign LQMO sectors to LQSA_APP in case Sarajevo Radar is online and there
  are no LQMO stations connected. This is to make it easier to implement our idea of covering all BiH airports procedurally
  from LQSA_APP when no other stations are connected. This behaviour can be overriden manually in ES via the Active Airport
  selector window and the Sector ownership menu.

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
  **Required minimum vis ranges** to match the preset centers: APP: 99 nm; TWR: 35 nm; GND: 10 nm. Approximate visibility radius
  around LQSA with these settings is: GND: 18nm, TWR: 60nm, APP: 150nm. Vis centers can always be overriden in ES.
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
* added parking position designators for all major and minor stands that can be shown or hidden individually
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

