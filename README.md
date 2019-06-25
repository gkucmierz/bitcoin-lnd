# bitcoin-lnd

## install bitcoind
```
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:bitcoin/bitcoin
sudo apt-get update
sudo apt-get install bitcoin-qt bitcoind
```

## config bitcoin
```
apt-get install nano
nano .bitcoin/bitcoin.conf
contab -e
* * * * * bitcoind
```

## running bitcoin node
```bitcoind```

### watch blocks syncing process
```
watch -n1 bitcoin-cli getblockcount
```
or:
```
apt-get install jq bc
watch -n1 echo "$(printf "%.2f" $(echo "100 * $(bitcoin-cli getblockchaininfo | jq '.verificationprogress')" | bc))%   blockcount: $(bitcoin-cli getblockcount)"
```

## installing bitcoin explorer (optional)
```
apt-get install git nodejs npm
npm install -g n
n stable
git clone https://github.com/bitpay/bitcore.git && cd bitcore
npm i
...
```
