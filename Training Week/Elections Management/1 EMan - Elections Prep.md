# Election Preparation

## Property Management

Property management should be the responsibility of the Gazetteer custodian, however is often done by the LA.

### Importing amends

`Wizards` > `Gazetteer Wizard`

* Can import changes, or
* Import entire Gazetteer.
  * Only usually used in on-boarding.
* There is an agreed upon national file format.

1. Open wizard.
    * Checks for compatibility, e.g. area.
      * *Errors* prevent proceeding.
      * *Warnings* allow continuation.
1. Import the file.
1. Work through Add/Amend/Remove
    * `Right click` > `Accept` or `Reject`.
    * `Right click` > `Accept For` allows to accept all changes with a specific type within the import file.

### Manual management

`Addressing` > `Street Maintenance`

* Shows all streets.
* `Double click` to see details/properties.
  * Gazetteer data has detailed data.
  * *Street Descriptor* is the street name.
* Use *Gazetteer Address* tab to change the address.
  * *PAO* is the *Primary Address Object*, the "Physical Footprint" of an address, i.e the building shell.
  * *SAO* is the *Secondary Address Object*, the actual property (e.g. a residence or a business) within a *PAO*.  Each *SAO* has a *UPRN*.
  * Changes will require a re-sequence of the register.
  
## Election preparation

There is an Election Management step-by-step guide on Zendesk

### Election types

`System` > `Manage election types`

* Shows all available election types.
* Tick box to enable election and options associated to that type in various other parts of the application.
* If election type is marked as in use, Electoral Areas need setting up.

### Creating Electoral Areas

`Elections` > `Electoral Areas`

* Shows all electoral areas for election type.
* `Right click` > `New Electoral Area`.
* Add a name, code and number of seats.
  * Code is important.
  * Enter number of seats here rather than in the election type settings.

#### Set Polling Districts

`Addressing` > `Polling Districts & Electoral Areas`

* Set the electoral area for each PD.
  * Use *Not in use* when PD does not vote in this Election Type.
  * Press *Assign All Districts to X* if all PDs in one area (e.g. European Parliament Elections).

`Wizards` > `New Election Wizard`

* The start of the wizard performs preflight checks.
* Run these checks regularly to ensure that PDs and Electoral Areas are setup correctly.

#### Area relationships

* *Election Type* contains
* *Electoral Area(s)*, which contains
* *Polling Districts*, which contain
* *Streets*, which contain
* *Households*, which contain
* *Electors*.

## Election timetable

`System` > `Manage Election Timetable`

* Shows events for election types
* Event types:
  * Statutory - mandatory, publicly visible.
  * Working Practise - other non-mandatory events and non-public events (e.g. printing).
* *Modifier* - date when event happens:
  * `0` is polling day.
  * Negative is the number of working days before polling day.
  * Positive is the number of working days after polling day.
* *Final Time* is the deadline time on the event day.
* *Time Deadline Notes* is the human readable description for the *Final Time* (for use on literature etc.)

`Elections` > `Manage Elections Timetable`

* Select a possible election date.
* Shows a calendar to show when events would happen.
  * Orange - Event.
  * Black - Non working dates.
* Can only have have one election of the same type active at a time.

### Deleting an election

1. `Elections` > `Manage Elections`
    * This should be restricted to administrators
1. `Right-click` > `Delete`.
