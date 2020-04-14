# Performing Boundary Changes

## Boundaries

In rough size order

* Polling Districts (PD)
* Parish/Community/Town Council ward
* District/Borough Council ward
* Parish Community Council Area
* County Division
* District/Borough Council Area
* Unitary Council Area - Scottish Councils and some English and Welsh Authorities
* Scottish Parliamentary Constituency/ies
* welsh assembly constituency/ies
* UK Parliamentary Constituency/ies
* Scottish VJB Council Areas - Registration Only
* Police & Crime Commissioner (PCC)
Mayoral
Greater London Assembly (GLA)
Counting Areas for Referendums

Neighbourhood Planning Referendums (NPR) - Can be any size (including a few houses).

## Changes

From

* Boundary Commission for Parliamentary,
* Local Government Boundary Commission,
* Local Authority,
* Community governance reviews for those with Community or Parish Councils,
* Polling district reviews - Statutory requirement (5 years).

Run on projected electorate figures projected for 5 years time to futureproof changes.

## Why

* Resolve electoral inequality (number of electors per councillor, +/- 10% allowed).
* Support effective and convenient government - increase/decrease the number of councillors/wards.

## In Elector8

* `Addressing` > `Manage Polling Districts` to do most management functions.
* `Addressing` > `Polling Districts & Electoral Areas` to see which PDs are used for different elections.

## Managing PDs via shape files

### Viewing polling districts

* `Addressing` > `Manage Polling Districts`
* Tab shows properties thought to be in the wrong Polling District
* *View Polling Districts* -> Map with live stats.
* `Right click` > `New District` to add new PD.
  * Can choose polling place or leave to set later.
* `Right click` > `Delete` to remove PD.
  * If the PD is not empty, you will be asked to move properties to another PD.
  * Merge PDs by deleting one.

### Viewing electoral areas

`Elections` > `Electoral Areas`

* `Right click` > `New Electoral Area` to create a new electoral area.
  * An electoral area can have multiple electable seats.
* `Right click` > `Delete Electoral Area` to delete area.
  * There is no warning before the delete happens.

`Addressing` > `Polling Districts & Electoral Areas`

1. Select *Election type*
1. Find polling district, select *Electoral Area*.

### Boundary Analyser

`Elections` > `Boundary Analyser`

* A "what if" tool.
* Requires PD shape files imported.
* *Show properties* shows the property distribution across a PD.
* *Show polling places* plots polling places if their position is known.
* Can print current view.

#### Drawing boundaries

1. Select starting area.
1. Select *Boundary changes* and then *Start*.
1. Draw new shapes to add to area.
1. Press *Finish*.

This then shows what affect the changes would make to the voter distribution.

* Doesn't affect live data.
* You have the ability to add properties at a point on the map - future property development.
* This is often then sent to the CAG/GIS team for finalising.

#### Importing boundaries

`Wizards` > `Polling District Boundary Import Wizard`

* Use wizard to import shape files.

### Updating the register

`Addressing` > `Manage Polling Districts`

* Shows properties in the wrong PDs.
* Imported/Analyser changes will appear as a property's *Potential polling district*.
* `Right click` > `Set suggested potential polling district` to change the PD.
  * This is a live change and will require the register to be resequenced and so should only be done at canvas.

`Electors & Registers` > `Manage Registers`

* Select *As published on* and *Use potential new polling districts*.
* This now shows the register with changes in purple.

`Addressing` > `Manage Polling Districts`

* `Right click` > `Accept suggested polling district for selected records` to make changes permanent.
  * This is a live change and will require the register to be resequenced and so should only be done at canvas.
* *Polling districts* tab, `right click` > `Resequence register`.
  * This causes live changes to the register and so causes issues for anyone using the register (including the open register).
  * Should only be done at canvas.

## Managing PDs without shape files

1. In `Addressing` > `Manage Polling Districts`, create new PDs.
1. In `Addressing` > `Street maintenance`, `right click` > `Set potential polling districts for all properties in street`.
    * Or double click to select on a property my property basis.
    * Shows all houses as moved, but only actually does selected ones.
1. `Right click` > `Apply potential new polling districts to the register`.
    * This is a live change and will require the register to be resequenced and so should only be done at canvas.

## Using the wizard

`Wizards` > `New Polling District Wizard`.

* This causes live changes to be made and will require the register to be resequenced and so should only be done at canvas.
