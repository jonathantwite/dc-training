# Elector Journey: Elector Determination

* Hopefully most people will use the Government's *Register to vote* website.

## With IERDS

`Electors & Registers` > `Manage Web Applications to Register`

* Use `Settings` > `Verification downloaded` to set auto download (often 1am).
* Can do a manual download.
* Unprocessed are those not uet matched to DWP data.

Suggested order to work through applications:

1) *Ordinary & Address Unmatched* tab.

* These then go into other tabs.
* Green - Verified.
* Red - Failed verification.
* Dark Red - Potentially fraudulent (high number of NINO usage).
* White - Unprocessed.

2) *Address Unmatched* tab.

* Addresses not found.
* Uses LLPG database or CAG (Scotland).
* If a user selects their address on the Government website, the address should match.  If they added their address manually, it usually doesn't.
* `Right click` > `Manually Find Address` and search for address.
* If you can't find address, `right click` > `Pending Reason` and add a note.
* *Pending Reasons* column is used to add notes as to what is being done to match the address.

3) *Address Matched*

* To match people so there are no duplicates on register.
* All possible matches are created when the data is downloaded.
* Two possible approaches:
    1. Individually,
        * If records are the same, `right click` > `Accept Possible Match on Selected`.
        * If no match, `double click` *Possible Existing Elector* field to see a dropdown with possibilities.
        * Finally, `right click` > `Add Selected Electors to the Database` > `Without Using The New Elector Wizard`.
    2. In bulk,
        * Select all records, `right click` > `Add Selected Electors to the Database` > `Without Using The New Elector Wizard`.
        * This only does the records with no possible matches.
* Matches are very loose and shouldn't miss anyone.
* All records post IER will have a date of birth, those from before often do not.
* Applications from existing ordinary voters are a match if a perfect match on:
  * Forename,
  * Middle name,
  * Surname,
  * Date of birth and
  * UPRN.
* These can be automatically processed.
* Can `right click` > `Update Verification status for this elector`.
  * This can only improve an elector's verification status.

### Deleting records

1. `Right click` > `Mark as no action`.  Add a reason.
    * Moved to *Applications marked as no action* tab.
1. `Right click` > `Permanently delete selected records`.

## From paper applications

`Communications` > `Scanning`

1. Select document type as *ITR*.
1. Add scan file, add to a batch or create a new batch.
1. Go to *Manage Batches*, `double click` on the batch, `double click` on the scan.
    * You can now edit data.
      * *Nationality* is limited by *Nationality Status*.
    * Can add previous address to start process of notifying previous authority.
    * Snippets are not kept as they are only needed to input the data correctly.

You can `right click` > `Quality Check This Document` on the scan row to perform a check on whether the form has been imputed correctly.

## Using Elector determination workflow

`Wizards` > `ITR Extract Wizard`

* For green electors, send confirmation letter.
  * Same options as for sending an ITR.
  * Print / Export to csv (for printers).
* Filter by date authenticated/added.
* Can exclude draft electors
  * i.e. Only send once added to register.

## For red electors

* Send a query letter if no DoB or NINO.
* Send documentation required letter if ITF perfect by failed verification.
* Some clients do not use query letters as they don't want to have to send both.

`Electors & Registers` > `Elector Determination`

* Different clients have different tabs.
* *Documentary Evidence Due* tab - waiting for elector to send documentary evidence.
* `Right click` > `Send communication`
  * Progress records through workflow by sending communcation.
  * Select *Elector Determination* and press *Load*.
    * Green: Ok,
    * Grey: Nothing to send currently,
    * Red: No letter in system to send.
  * *Last Item* / *Next Item* to work through workflow steps.
  * *Communication Template* shows letter to send.
    * Can be set up in workflow.
    * If multiple templates available, forces user to choose.
    * If only one template of type, uses that one.
    * `Right click` to apply to all records in this batch.
  * Records now move to *Documentary Eveidence Sent* tab.
