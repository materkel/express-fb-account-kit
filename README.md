**|| In Development**

# express-fb-account-kit
Integrate Facebook Account Kit with expressJS

## Usage

```js
const express = require('express');
const AccountKit = require('mfressdorf/express-fb-account-kit')({
  appId: 'YOUR_APP_ID',
  appSecret: 'YOUR_APP_SECRET'
}) // Not on NPM yet!

const app = express();
app.use('auth', AccountKit.setup());
app.use(AccountKit.validate());

app.get('secretPath', (req, res) => {
  // should only be visible for registered account kit users
});

app.listen(3000);
```
