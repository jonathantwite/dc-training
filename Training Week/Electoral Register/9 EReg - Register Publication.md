# Register Publication

* 1 December:
  * Annual refresh.
  * New numbers.
  * Must communicate to interested parties.
* Monthly:
  * Just changes (NOA).
* Three times leading up to an election:
  * As monthly.

## Prepublish process

### Interested parties

`Electors & Registers` > `Interested Parties`

* Different people want register in different formats and at different frequencies.
* Elector8 then automates the sending of the register to interested parties.
* Record colours:
  * Green: Previous record send ok.
  * Red: Previous record failed.
  * White: No previous attempt.
  * Blue: Scheduled to send.

#### Create a new interested party

`Right click` > `New Interested Party`

1. Can set a department if multiple records needed by the same organisation.
1. Set their reference.
1. Set how to deliver the their copy of the register:
    * Council FTP (interested party downloads),
    * Recipient's FTP,
    * Emailed `.zip` file,
    * Posted `.zip` file - for creating a USB drive (or similar), or
    * Local disk - especially for printing.
1. Select extracts (usually NOA or Annual register):
    * NOA,
    * Register to NOA - register as changed by all NOAs up to now,
    * Annual register, or
    * All other publications.
1. Must enter an email address regardless of sending method.
1. If `.zip` file selected, the password must score *Strong* or *Very strong*.

#### Setting up the new interested party

After adding a new *interested party*:

`Right click` > `Change settings`

* Select electoral areas to send.
* *Save each polling district separately* creates separates files for each PD.
* Can use custom name or automatically generated names.
* Selecting to show *Deletions* also includes deaths.
* *Edited Register* is actually the *Open Register*.
  * Credit reference agencies get the full register with *Opt out* flag added.
  * The Jury Service (Jury Central Summoning Bureau?) require *Court Markers* flag (shows people eligible for jury service).
* Select format from `.pdf`, `.csv` or *Excel*.
* The *Fixed Format Extract Settings Tab* has preset file formats from different bodies.

#### Viewing an extract

In the *Interested parties* screen

* `Right click` > `View Amendments To The Register`.
  * Shows all unpublished future amendments.
  * Can change the date when a change is published.
  * `Right click` > `Change Elector From Draft to Full Elector` - only some people use this.

## Register dates

`System` > `Regional Settings`

*Register Dates* tab.

Phase Date
: Publication date.

Application Deadline
: Date by when applications must have been made.
  Usually 1st week of previous month.

Determination Deadline
: Date by when applications must have been confirmed (verified).
  Often one week after *Application deadline*.
  For annual publication and elections, usually day before publication.

### Example

|Publication Date|Application Deadline|Determination Deadline|
|---|---|---|
| 1 March|5 February|15 February|
| 1 April|5 March|15 March|
| 1 May|5 April|15 April|
| 4 May|28 April|3 May|

* 4th May publication is probably for an election as *Determination deadline* is day before.

<!-- markdownlint-disable MD033 -->
|Communication received|Date first on register|
|---|---|
|ITR received 4 March (Red)<br />Evidence received 18 March|1 May|
|Change of name with evidence received 2 May|4 May|
|ITR received 8 March (Green)|1 May|
|Paper ITR received 4 February<br />IERDS returned green 11 February|1 March|
<!-- markdownlint-enable MD033 -->

## Publication

`Wizards` > `Publish Register Wizard`

1. Does validation checks.
    * Recommend keep coming into this screen prior to publication day to check that all of the pre-requisite tests pass.
1. Select reason - which publication.
1. Shows related dates.
1. Can select specific PDs.
    * Usually for elections where there are only some PDs taking part - however, Elector8 does this automatically.
    * Shows drafts - watch number so that it doesn't get too high.
1. Can remove electors with expired reviews & hearings at this point.
1. Confirm that a backup has been taken.
1. Asks whether to resequence.
    * Only ever done on the Annual publish.
1. The *Non register amendments tab* shows changes that don't change the register (e.g. email address).
1. The wizard then sends emails to *Interested parties*.
    * Option to produce reports or extra copies.

## Discretionary  and adhoc registers

`Electors & Registers` > `Manage Registers`

* Can select register *As published on* or *current*.
* Can choose *Current PDs*, *Potential new PDs* or *Previous PDs*.
* Select output type.
* Under *Governance*, select the type of election.
  * This affects, for example, the age range used (15+ for Scottish Assembly).
* *Formatting* tab has output format settings as previous.
* *Sales* tab allows creation of a new sale.
  * Can use a price caluculation:
    * Flat fee,
    * Per PD, or
    * Fee + Per person (usually used).
