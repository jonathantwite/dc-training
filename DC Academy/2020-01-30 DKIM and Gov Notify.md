# Emails, DKIM and Gov.Notify

`Regional Settings` > `Email Service`

* Email is insecure.
* Elector8 makes API call to DC's UKFast server, with credentials as set here.
* Then sent via an SMTP server.
* `Elector8.exe.config` communication service section, has the `.svc` endpoint details.

## DKIM

* DomainKeys Identified Mail
* Way to authenticate domain is legitimate and email is actually from that domain.
* Public/Private key encryption system.
* Public key sent with email to prove authorship
* Mail includes `DKIM-Signature` header with:
  * Domain and Selector Record details.
  * Hash of headers and body.
* ISP or email program can then retrieve the public key from the domain and verify the email.

## DMARC

* Domain-based Message Authentication Reporting and Conformance.
* Protocol which controls what happens if an email fails verification.
* Very strong Government recommendation to use DMARC to secure council emails.

## SPF

* Sender Policy Framework
* List of approved IPs that can send an email purporting to be from a specific domain.
* Used to check that an email has come from a computer authorised to send on behalf of a domain.

## Setup

* Emails from Elector8 need to impersonate the client's email domain.
* Client needs to add an SPF record for DC's email server.
  * Otherwise emails may be blocked randomly by ISP and DC will have no sight over which ones fail.
* Zendesk article *Setting up DMARC and DKIM for email sending* goes through the process.
  * They will need to create a public/private key pair (e.g. using *OpenSSL*) and enter the values into Elector8.
  * DKIM selector key should be called democracycounts.
* *mxtoolbox* and *dkim-inspector* are online tools useful for inspecting that the setup has been done correctly.

## Gov.Notify

<https://www.notifications.service.gov.uk/>

* Central Government-provided system for sending communications.
* Only available for organisations with a `.gov.uk` domain address.
* Can use `.csv` files or be directly integrated into via API.
* DMARC and DKIM automatically applied as emails will come from a `.gov.uk` registered IP.
* Cheap - 25k text messages per user free per year
* Emails, texts and A4 letters.
  * Letters are ~30p each.
* Organisations can create delegated accounts for users outside their organisation (e.g. DC).
  * What pages a user can see can be defined.
* Pages:
  * Dashboard - sent, failures etc.
  * Templates - Create template for email/text/letter.
  * Team members - user creation.
  * Usage - top up etc.
  * Settings
  * API Integration - create an API key
* There is an enforced trial mode first, including for all new API integrations.  This can be full trial (no communications sent) or send to registered users only.
* In Elector8, `Regional Settings` > `NotifyAPIKey` to set API key.

### New templates

1. On Website:
    * New template page shows formatting - like markdown.
    * Placeholders are in ((double brackets)).
1. In Elector8:
    * Create communication template.
    * Select *Notify email* (etc.) sending method.
    * *Notify Email* tab now appears.
    * Dropdown reads from API to get all available templates.
    * Reads all placeholders and shows a dropdown for each one to select an Elector8 field.
    * Communications sent in the normal way.

* Note, uses government hardware so no control over speed of sending.

### Attachments

* Setup as normal
* User placeholder - this will become a link to a secure file location on gov.uk servers.
* Can setup up to 5 attachments.
* Add the attachments to the attachment box in Elector8 template editor.
* Select *Attachment 1* etc. from the placeholder mapping dropdown.
