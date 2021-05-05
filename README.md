# ![LOGO](logo.png) sevDesk Contact API OIH Connector

## Description

[![Generic badge](https://img.shields.io/badge/Status-NotTested!-lightgrey.svg)](https://shields.io/)

A generated OIH connector for the sevDesk Contact API (version 2.0.0).

Generated from: https://my.sevdesk.de/api/v1<br/>
Generated at: 2021-04-22T22:41:51+02:00

## API Description

## Authorization

Supported authorization schemes:

- API Key

## Actions

### Get next free customer number

> Retrieves the next available customer number. Avoids duplicates.<br/>

_Tags:_ `Contact`

### Check if a customer number is available

> Checks if a given customer number is available or already used.<br/>

_Tags:_ `Contact`

#### Input Parameters

- `customerNumber` - _optional_ - The customer number to be checked.<br/>

### Retrieve contacts

> There are a multitude of parameter which can be used to filter.<br><br/> > <br/>
> A few of them are attached but<br/> > <br/>
> for a complete list please check out <a href='https://5677.extern.sevdesk.dev/apiOverview/index.html#/doc-contacts#filtering'>this</a> list<br/>

_Tags:_ `Contact`

#### Input Parameters

- `depth` - _optional_ - Defines if both organizations <b>and</b> persons should be returned.<br><br/>
  <br/>
  '0' -> only organizations, '1' -> organizations and persons<br/>
  Possible values: 0, 1.
- `customerNumber` - _optional_ - Retrieve all contacts with this customer number<br/>

### Create a new contact

> Creates a new contact.<br><br/> > <br/>
> For adding addresses and communication ways, you will need to use the ContactAddress and CommunicationWay endpoints.<br/>

_Tags:_ `Contact`

### Find contact by ID

> Returns a single contact<br/>

_Tags:_ `Contact`

#### Input Parameters

- `contactId` - _required_ - ID of contact to return<br/>

### Update an existing contact

> Update a contact<br/>

_Tags:_ `Contact`

#### Input Parameters

- `contactId` - _required_ - ID of contact to update<br/>

### Get communication ways of contact

> Returns all communication ways of a given contact.<br/>

_Tags:_ `Contact`

#### Input Parameters

- `contactId` - _required_ - ID of contact for which you want the communication ways<br/>

### Add phone number to contact

> Adds a phone number to a contact.<br/>

_Tags:_ `Contact`

#### Input Parameters

- `contactId` - _required_ - ID of contact to which phone number is added<br/>

### Add email to contact

> Adds an email to a contact.<br/>

_Tags:_ `Contact`

#### Input Parameters

- `contactId` - _required_ - ID of contact to which email is added<br/>

### Add address to contact

> Adds an address to a contact.<br/>

_Tags:_ `Contact`

#### Input Parameters

- `contactId` - _required_ - ID of contact to which address is added<br/>

### Create a new contact address

> Creates a new contact address.<br/>

_Tags:_ `ContactAddress`

### Retrieve communication ways

> Returns all communication ways which have been added up until now. Filters can be added.<br/>

_Tags:_ `CommunicationWay`

#### Input Parameters

- `contact[id]` - _optional_ - ID of contact for which you want the communication ways.<br/>
- `contact[objectName]` - _optional_ - Object name. Only needed if you also defined the ID of a contact.<br/>
- `type` - _optional_ - Type of the communication ways you want to get.<br/>
  Possible values: PHONE, EMAIL, WEB, MOBILE.
- `main` - _optional_ - Define if you only want the main communication way.<br/>
  Possible values: 0, 1.

### Create a new contact communication way

> Creates a new contact communication way.<br/>

_Tags:_ `CommunicationWay`

### Deletes a communication way

_Tags:_ `CommunicationWay`

#### Input Parameters

- `communicationWayId` - _required_ - Id of communication way resource to delete<br/>

### Create a new accounting contact

> Creates a new accounting contact.<br/>

_Tags:_ `AccountingContact`

## License

: sevDeskContacts-Component<br/>
<br/>

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
