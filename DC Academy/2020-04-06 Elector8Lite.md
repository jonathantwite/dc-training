# Elector8Lite

SharePoint > Support > DCL Product Support Documentation > Elector8Lite > Installation Guide

* Website running under IIS.
  * Customers should be installing IIS, but often don't feel confident doing so.
* Database connection uses SQL Authentication not Windows Authentication.
  * Need both Elector8 databases setup for this.

## SQL setup

In SQL Server Management Studio

* Allow mixed mode authentication
    1. `right-click` the database server > `Properties`, *Security* tab.
    1. Select *SQL Server and Windows Authentication mode*.
    1. Restart the SQL server - `right-click` on the server > `Restart`.
        * Client should be responsible for doing this as they may have other databases on that server.
* Create SQL login
    1. `Security` > `Logins` > `right-click` > `New Login`
        * Use `User ID = Elector8Lite` and `Password = D3m0@1234` as these are the default values in the application configuration file.
        * Disable password complexity setting.
        * Disable password policy setting.
    1. Click *Ok*.
    1. Open user > *User Mappings* tab.
    1. Add *Owner* and *Writer* permissions for both databases.
        * This creates the user in those databases.

## IIS installation

*Start menu* > *Control Panel* > *Programs and Features* > *Turn Windows Features On or Off*.

Required features:

* Internet Information Services
  * World Wide Web Services
    * Application Development Features
      * *.NET Extensibility 3.5*
      * *.NET Extensibility 4.7*
      * *ASP*
      * *ASP.Net 3.5*
      * *ASP.Net 4.7*
      * *ISAPI Extensions*
      * *ISAPI Filters*
    * Security
      * *Basic Authentication*
      * *Request Filtering*

This also installs Internet Information Services Manager.

## Installing Elector8Lite

1. Run `Elector8.msi`.
    * Adds the site to the default site in IISM.
1. Open `C:\inetpub\wwwroot\Elector8Lite\web.config`.
    * Connection strings have `User Id=...;Password=...;` instead of `Integrated Security=true;`.
    * Adjust the `Catalogue` names
    * Can use an encrypted password - ask dev team to set one up and adjust config file where shown.
1. Runs at <http://localhost/Elector8Lite>

## Notes

* Website uses *Forms Authentication*.
* Messages sent from Elector8Lite are added straight into the database.

## Elector8 link

`System` > `Regional Settings`

* Set the *Elector8Lite Url* to the url used.
  * Allows multiple people to use Elector8 for simple (usually phone-based) enquiries.

`System` > `Elector8Lite Settings`

* User must exist in a group (`System` > `User Groups`).
* Can select options visible for different groups of people.
* Can create a landing screen.
