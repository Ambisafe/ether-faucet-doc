<a href="https://www.ambisafe.co/">![test](img/logo_red.png)</a>
**********
# Ether Fauset

Wallet funding utility.

Service deployed on <https://faucet.ambisafe.co>

**********

## API usage

**POST /dispense** with header **Authorization: [JWT faucet token]** and body:
```json
{
	"to": "your ethereum address",
	"amount": 10000000000000000
}
```

will give 0.01 Ether from the Treasury and this response:

```
{
	"hash":"0xa447d3d1ae45896a7afdd6b700ee7e38646d3178a4356f2358c5fb688a0b3812"
}
```

## JWT faucet token
```js
{
	"iss": API_KEY,
	"jti": uuid4,
	"sub": "faucet",
	"aud": "ambisafe",
	"exp": expirationDate
}
```
Should be signed with your API_SECRET
