# Register Accuracy

## Logging Removal Evidence

1. Find the person with the person search.
    * If notification received via a letter or email, record communication as *Unsolicited Email*.
1. On the *Person* details screen, `right click` > `Remove Voter`.  Select *Summary removal*.
    * 'Delete' Option is used when there has been an administration error.
    * User 'Mark as deceased' if the voter has died.
1. Select *First source of evidence*.
1. Click *Next*, this creates a *Partial summary removal*.
1. Create a review is wanted (usually *Type A*).
1. Often you would now send a communication.

* To see partial summary removals, `Electors & Registers` > `Incomplete Partial Summary Removals`.
  * Search function available.
  * `Right click` > `Elector Details` opens a popup with the *Person screen*.
* Can remove multiple electors from the household screen.
* Can `right click` > `Record as person of interest`.

## Reviewing Records

To mark a person for review:

1. In the *Person* screen, `right click` > `Mark for review`.
1. Select type and reason.  This is now visible on the *Person* screen.

To remove a *Partial summary removal*:

1. In the *Person screen*, `right click` > `Remove summary removal`.

To update and complete:

1. In the *Person screen*, `right click` > `Summary removal`.
1. Add a second source of evidence.
    * Can overwrite an existing piece of evidence if needed.
1. Click *Next* and select *Yes*.  This archives the elector.

## Reviews

`Electors & Registers` > `All Reviews, Objections & Hearings`

* Shows all reviews
* *Determination Date* is calculated from *start date* and *type*.
  * *Type A*: 14 days.
  * *Type B*: 28 days.
  * *Type C*: 7 days.
* View defaults to showing all current electors.
  * Green: New.
  * White: On register.
  * Red: Archived.
* `Right click` > `Edit` to record hearing date or edit type.
* `Right click` > `Send communications` to send a communication.
* To end an objection, `right click` and select either:
  * `Remove elector` - removes elector from register.
  * `Review successful - elector to remain` - elector remains on register, or
  * `Reinstate` - reinstate an archived elector.
* Poll cards can be prevented from being sent via `right click` > `Suppress poll card for selected elector`.
* Reviews can be exported.
* Objections tab has similar options.

## Managing duplicates

`Electors & Registers` > `Duplicate Electors`

* Four tabs:
  * **Duplicates at previous address** - usually person has moved.
  * **Duplicates in same household** - often two people with the same name in the family.
  * **Duplicates in the same household with same forename** - again, often two people with the same name in the family.
  * **Duplicates at other addresses** - often due to a person moving but not informing LA so that the process has not been followed.
* Duplicates often caused by the middle name being added.
* Right-click options are slightly different for each tab.
* For *Other addresses* tab,
  * `View Elector 1 household`,
  * `View Elector 2 household`,
  * Can see each elector details.
* Once sure that they are the same person, `right click` > `Remove elector 1` or `Remove elector 2`.
  * Starts a summary removal.
* Other options are `Mark electors as separate people` and `Mark property as a must canvass`.

## Tell Us Once

* Mainly used for deaths.
* Has a service to download notifications.
* If only one or two,
    1. Add notification to household as a *Deceased notification*.
    1. Removal wizard starts, select to mark as deceased.
* For regular bulk imports, use *Insite*
  * Data warehousing application.
* For infrequent bulk, use `Wizards` > `Bulk Additions & Deletions`.
    1. Import file
        * File needs editing to have *ADD*, *DELETE* or *DECEASED* in an initial column.
        * Usually all of one type.
    1. Map columns to *Elector8* database columns.
        * Do not need to use *ADD* / *DELETE* column as this is automatically read.
        * Can cope with just *Address Line 1* and *Postcode* to match address.
    1. Summary of all imports shown.
    1. Can finish wizard and then manage changes in `Electors & Registers` > `Bulk Additions and Deletions`.
    1. In *Matched Additions* tab, `right click` > `Add Selected Elector to Database` > `Without Using New Elector Wizard`.
    1. In *Unmatched Additions* tab, search for address for each record.
    1. Follow similar process for *Deletions* and *Deaths*.
