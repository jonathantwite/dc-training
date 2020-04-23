# Gazetteer Import Process

`Wizards` > `Gazetteer Wizard`

* Add/Modify/Delete streets, then
* Add/Modify/Delete properties.

* Two options
  * Import a *Change Only* file (COU file).
    * Elector8 can watch a file location or user can manually import a file.
    * Must be imported chronologically
    * Uses *BS7666* standard.
  * Use entire Gazetteer file as an update.
    * Updates an existing database with the complete Gazetteer data.
    * Uses a *DTF7.3* format file.
    * Recommended to be done six-monthly.
* Files are also sent to the Cabinet Office and so used for the GDS, including *Register to Vote*.

1. Select Gazetteer file
    * Shows the number of rows read.
1. Select *Next*, runs various checks.
    * Errors are blocking, warnings are not.
    * Warnings are validation errors, validating the file against the *BS7666* standard.
    * Double click to see more details (location in file etc.)
    * Warnings should be flagged to the Gazetteer Custodian.
    * *Record summary* tab shows the summary with respect the the *BS7666* standard.
1. Select *Next*, loads file into database DTF tables.
1. Select *Next*, shows new streets.
    * Can show previously rejected changes.
    * *Lang* column used as Welsh streets will have two records.
    * Residential properties are calculated from later in the file.
    * When loaded for the first time, automatically selects streets with one or more residential properties.
    * `Right-click` > `Accept Selected New Streets`.
    * Can map to an existing street.
      * When a new street is known about but not yet in the Gazetteer, LAs will often create the new street in Elector8 with a negative USRN.  Use the mapping function to map street additions in the Gazetteer to these negative USRNs, replacing them with the now-known details.
1. Select *Next*.  No changes are made to the database at this point.  Shows street updates.
    * For example, town name correction.
    * Can `right-click` > `Export All Records`.
1. Select *Next*, shows street deletions.
    * No street can be deleted while properties remain on it.
    * Empty streets will automatically selected.
1. Select *Next*, shows property additions.
    * Compares location with Polling Districts to see if it can auto assign one.
        1. If street has a single PD, use that PD
        1. If a street has two or more PDs, use the house numbers to see if surrounding houses have the same PD.  If so, use that PD.
        1. Otherwise try the geographic location to suggest a PD.
1. Select *Next*, shows property deletions
    * As with other screens, only flags for deletion.
1. Select *Next*, shows LPI deletions.
    * E.g. House and business at single address become a single residential property.
1. Select *Next*, shows property updates.
1. Select *Next*, shows a summary of changes.
    * Select *View* to return to the specific change screen.
1. Select *Next* to save changes.
1. Select *Next*, shows a screen to set canvas campaign groups for new and altered properties.
1. Select *Finish*.

`Addressing` > `Gazetteer Imports`

* This screen shows the streets/properties excluded during the wizard and can be added from here.
* Useful if a street was believed to be commercial-only, but was later found to have a residential property that needs adding.
