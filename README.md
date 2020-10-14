countrylist
==============================
Basic library for Country, State and City

Initial database fetched from: https://github.com/hiiamrohit/Countries-States-Cities-database
Improved and updated Repo from: https://github.com/harpreetkhalsagtbit/country-state-city

# Installation
`npm i countrylist`


# Integration
  - ES6 Module usage
   
     ```js
     import csc from 'countrylist'

     // Import Interfaces`
     import { ICountry, IState, ICity } from 'countrylist'
     ```
  - AMD Module usage
  
    ```js
    let csc = require('countrylist').default

    // OR

    let csc = require('countrylist')
    ```


# Documentation

getCountryByCode(code)
---------------

It accepts a valid `CountryCode` (sortname) eg: `'AS'` and   returns *Country Details*

type: **json | ICountry**

example: **getCountryByCode(AS)**

```js
{
	"id": "4",
	"sortname": "AS",
	"name": "American Samoa",
	"phonecode": "1684"
}
```

getCountryById(id)
---------------

It accepts a valid `CountryId` and   returns *Country Details*

type: **json | ICountry**

example: **getCountryById(4)**

```js
{
	"id": "4",
	"sortname": "AS",
	"name": "American Samoa",
	"phonecode": "1684"
}
```

getStateById(id)
---------------

It accepts a valid `StateId` and   returns *State Details*

type: **json | IState**

example: **getStateById(4119)**

```js
{
	"id": 4119,
	"name": "Midlands",
	"country_id": "246"
}
```

getCityById(id)
---------------

It accepts a valid `CityId` and   returns *City Details*

type: **json | ICity**

example: **getCityById(3)**

```js
{
	"id": "3",
	"name": "Port Blair",
	"state_id": "1"
}
```

getStatesOfCountry(countryId)
---------------

It accepts a valid `CountryId` and   returns *all States* as Array of JSON

type: **array of json | IState**

```js
[
  {
    "id": 4119,
    "name": "Midlands",
    "country_id": "246"
  }
]

```
getCitiesOfState(stateId)
---------------

It accepts a valid `CityId` and   returns *all Cities* as Array of JSON

type: **array of json | ICity**

```js
[
  {
    "id": "3",
    "name": "Port Blair",
    "state_id": "1"
  }
]

```

getAllCountries
---------------
It returns **all Countries**

type: **array of json | ICountry**

```js
[
  {
    "id": "4",
    "sortname": "AS",
    "name": "American Samoa",
    "phonecode": "1684"
  }
]
```
