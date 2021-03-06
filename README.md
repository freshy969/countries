# Countries

Countries supported by Paylike. Sorted alphabetically.

Notice that this has nothing to do with accepting cards. Cards from all over
the world are accepted.

You will need a registered company or citizenship from one of these countries:

- Austria
- Belgium
- Bulgaria
- Croatia
- Cyprus
- Czech Republic
- Denmark
- Estonia
- Faroe Islands
- Finland
- France
- Germany
- Gibraltar
- Greece
- Greenland
- Hungary
- Iceland
- Ireland
- Italy
- Latvia
- Lichtenstein
- Lithuania
- Luxembourg
- Malta
- Monaco
- Netherlands
- Norway
- Poland
- Portugal
- Romania
- San Marino
- Slovakia
- Slovenia
- Spain
- Sweden
- Switzerland
- United Kingdom

## Usage

Pin the dependency to the current version branch to ensure future installs of
your application will work. Like so:

```json
"dependencies": {
	"@paylike/countries": "*"
}
```

```js
var countries = require('@paylike/countries');

countries;
/*
[
	{ code: 'AT', currency: 'EUR', name: 'Austria' },
	{ code: 'BE', currency: 'EUR', name: 'Belgium' },
	...
]
*/

countries.find(c => c.code === 'DK');
// { code: 'DK', currency: 'DKK', name: 'Denmark' }

// countries with EUR as default
countries
	.filter(c => c.currency === 'EUR')
	.map(c => c.name);
```

Notice that some countries are primarily using EUR online although they have a
distinct domestic currency. An example is Romania in which you might prefer a
merchant account in EUR over RON.
