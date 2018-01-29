# Coal-js
![](fire.jpg)
The JavaScript API Client for LocomotiveCMS V3 (WIP).

## Installation

```bash
npm install coal-js
```

## Usage

```
Client = require('./coal/client.js').Client;

const client = new Client({
  baseUrl: "https://station.locomotive.works/locomotive/api/v3",
  email: "ruben.cunha@gmail.com",
  apiKey: "bcc74aeff61f5c6735884a51024db81c882b6ed4"
});

// get user name
client.getMyAccount()
  .then(({data}) => console.log(data.name))

// get site name
client.getSites()
  .then(({data}) => console.log(data[0].name))
```

## NPM Scripts

``` bash
# install dependencies
npm install

# run tests
npm run test

# run one single test
npm run test:single ./src/coal/client.test.js

# run tests and watches for file changes
npm run dev

# run tests and launch node-inspector to debug with chrome-devtools (https://medium.com/@paul_irish/debugging-node-js-nightlies-with-chrome-devtools-7c4a1b95ae27)
npm run debug

# build dist for production (ES5)
npm run build
```

## Roadmap

* [x] POST /tokens.json
* [x] GET /my_account.json
* [x] GET /sites.json
* [ ] POST /sites.json
* [ ] DELETE /sites.json/{id}
* [ ] GET /pages.json
* [ ] GET /pages.json/{id}
* [ ] POST /pages.json
* [ ] PATCH /pages.json/{id}
* [ ] DELETE /pages.json/{id}
* [ ] GET /content_types.json
* [ ] GET /content_entries.json
* [ ] GET /content_entries.json/{id}
* [ ] POST /content_entries.json
* [ ] PATCH /content_entries.json/{id}
* [ ] DELETE /content_entries.json/{id}
