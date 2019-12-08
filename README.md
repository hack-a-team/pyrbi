# pyrbi
A simple python client for RBI blockchain's API

## Install

```
pip install pyrbi
```

## Usage

Initialize with
```python
from pyrbi import PyRBI
cli = PyRBI("user", "pass")
```

Then you can create wallet...
```python
cli.create_wallet()
```

```
{
  'pk': '0x98f5f0839c7645affac(...)f43',
  'pb': '0x3accd901450773a3fc4fd98ecf3b12(...)c4f530eff68554b806063bb6',
  'add': '0x8(...)6cEE0CbCcB9839e1c2',
  'mnemonic': 'expand focus ostrich(...)'
 }
 ```

Sync a wallet

```python
cli.sync_wallet("alerts", "0x8(...)6cEE0CbCcB9839e1c2")
```

```
{
  'status': 200,
  'data': '0xaf2c3a91e81b0980a6d638c7098a0ba9274476e3987eff5342d0e413a94cd3f4'
}
```

Put data into the wallet

```python
 cli.put_data("hello!", "0x8(...)6cEE0CbCcB9839e1c2", "0x98f5f0839c7645affac(...)f43")
```

```
{
  'status': 200,
  'data': '0x0a1fa838fede9(...)674a13cbb887424e2c66'
}
```

Retrieve data from the wallet

```python
cli.get_data("0x0a1fa838fede9(...)674a13cbb887424e2c66"):
```

```
hello!
```

## License

MIT
