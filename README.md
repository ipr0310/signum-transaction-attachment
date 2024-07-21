# Signum transaction attachment quick examples

See multiple examples of certain transaction's attachment. You may use this for any purpose. Research, development, etc...

I used it heavily when building the mobile wallet, multiple wallets and explorer also read these transaction attachments.

## Text message

```json
  "attachment": {
    "version.Message": 1,
    "message": "This can be a memo for a exchange or anything else",
    "messageIsText": true
  }
```

## Encrypted text message

```json
  "attachment": {
    "version.EncryptedMessage": 1,
    "encryptedMessage": {
      "data": "4a33b11d50bdf97aaff9b376597447d924c77f9ee25640642b28a2a93c326220e0cbdc39b3f950155a328b8b4034f9eeecfa5769a9766d962e57d3d9e748ebd4",
      "nonce": "a57860e9484de3359b3c2c825f351572a343b064bb54aa90ce0374b36b872c39",
      "isText": true
    }
  }
```

## Add commitment

```json
  "attachment": {
    "version.CommitmentAdd": 1,
    "amountNQT": 70000000000
  }
```

## Remove commitment

```json
  "attachment": {
    "version.CommitmentRemove": 1,
    "amountNQT": 5000000000000
  }
```

## Alias Assignment

### Signum TLD

```json
  "attachment": {
    "version.AliasAssignment": 2,
    "alias": "ipr0310",
    "uri": "",
    "tld": "0"
  }
```

### Nostr TLD

```json
  "attachment": {
    "version.AliasAssignment": 2,
    "alias": "ipr0310",
    "uri": "",
    "tld": "11970079337033010777"
  }
```

## Update account info

```json
  "attachment": {
    "version.AccountInfo": 1,
    "name": "ipr0310",
    "description": "hello world"
  }
```

## Alias Sell

### No Price (When there is not price in an alias sell, the alias gets transfered)

```json
  "attachment": {
    "version.AliasSell": 2,
    "alias": "2881696599904016237",
    "priceNQT": "0"
  }
```

## Buying an alias

```json
  "amountNQT": "10000000000",
  "attachment": {
    "version.AliasBuy": 1,
    "alias": "testbuy"
  }
```

## Token Creation

### VCRTHDPE

```json
  "attachment": {
    "version.AssetIssuance": 2,
    "name": "VCRTHDPE",
    "description": "Token issued and controlled by smart contract ID: 10133295301321529884",
    "decimals": 3,
    "mintable": true,
    "version.Message": 1,
    "message": "5643525448445045000000000000000000000000000000000000000000000000",
    "messageIsText": false,
    "quantityQNT": "0"
  }
```

### TTT1

```json
  "attachment": {
    "version.AssetIssuance": 2,
    "name": "TTT1",
    "description": "Shefs test token for liquidity pools testing. Mintable",
    "decimals": 1,
    "mintable": true,
    "quantityQNT": "10000000000"
  }
```

## Ask Order Placement (Sell order)

```json
  "attachment": {
    "version.AskOrderPlacement": 1,
    "asset": "15297368334901195317",
    "quantityQNT": "1900",
    "priceNQT": "2123456"
  }
```

## Bid Order Placement (Buy order)

```json
  "attachment": {
    "version.BidOrderPlacement": 1,
    "asset": "14029006807171356987",
    "quantityQNT": "4999000000",
    "priceNQT": "1"
  }
```

## Token Mint

```json
  "attachment": {
    "version.AssetMint": 1,
    "asset": "4650261435909806",
    "quantityQNT": "510"
  }
```

## Distribute to token holders

### **Send 75 SIGNA and 37 stTRT** to TRT holders having a minimum of 1,000 TRT

```json
  "amountNQT": "7500000000",
  "attachment": {
    "version.AssetDistributeToHolders": 1,
    "asset": "12402415494995249540",
    "quantityMinimumQNT": 10000000,
    "assetToDistribute": "14175641444126570597",
    "quantityQNT": "370000"
  }
```

### **No SIGNA sent, sent 23 stTRT** to TRT holders having a minimum of 2,000 TRT

```json
  "amountNQT": "0",
  "attachment": {
    "version.AssetDistributeToHolders": 1,
    "asset": "12402415494995249540",
    "quantityMinimumQNT": 20000000,
    "assetToDistribute": "14175641444126570597",
    "quantityQNT": "230000"
  }
```

### **759 SIGNA sent, No tokens sent** to TRT holders having a minimum of 3,000 TRT

```json
  "amountNQT": "75900000000",
  "attachment": {
    "version.AssetDistributeToHolders": 1,
    "asset": "15784340403242018732",
    "quantityMinimumQNT": 30000000,
    "assetToDistribute": "0",
    "quantityQNT": "0"
  }
```

## Token Transfer

### 1 SIGNA and 100 ZeroDigits sent

```json
  "amountNQT": "100000000",
  "attachment": {
    "version.AssetTransfer": 1,
    "asset": "10503474580484569331",
    "quantityQNT": "100"
  }
```

### No SIGNA sent 247,635 TokenY

```json
  "amountNQT": "0",
  "attachment": {
    "version.AssetTransfer": 1,
    "asset": "11740968825822987655",
    "quantityQNT": "247635304"
  }
```
