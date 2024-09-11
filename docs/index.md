
bitcoin-cli -conf=/data/bitcoin.conf stop
bitcoind -conf=/data/bitcoin.conf -daemon
bitcoin-cli -conf=/data/bitcoin.conf removemempoolentry 8833e0237b77a7ccdeda9731337c5fb8a09b1f71246ecc0528af2697b7d26207
bitcoin-cli -conf=/data/bitcoin.conf getrawmempool true


bitcoin-cli -conf=/data/bitcoin.conf getrawmempool true | grep -B 4 '"unbroadcast": true' | grep '"txid"' | awk -F'"' '{print $2}'
bitcoin-cli -conf=/data/bitcoin.conf getrawmempool true | grep -B 10 '"unbroadcast": true' | grep '^[ ]*"[^"]\+' | awk -F'"' '{print $2}'



rm /path/to/bitcoin/data/mempool.dat

yarn cli wallet balances -t https://tracker.catprotocol.org


#### bash 
```
#!/bin/bash

# 获取所有内存池中的交易 txid
txids=$(bitcoin-cli -conf=/data/bitcoin.conf getrawmempool)

# 遍历每个 txid 并移除交易
for txid in $txids
do
  # 过滤掉无效字符（去除 [ 和 ] 以及逗号）
  txid=$(echo $txid | tr -d '[]"',)
  
  # 打印要移除的交易 txid
  echo "Removing txid: $txid"

  # 移除交易
  bitcoin-cli -conf=/data/bitcoin.conf removemempoolentry $txid
done
```
#### 卡住的 tx
Minting 5.00 CAT tokens in txid: 02b4ee71ec226c3c972c85722376424441867297d083e998b47325cd9f2a1d00 ...
✨  Done in 1.79s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: b2e1da2aae8dfd94a3af50f46c761af7292741b749172a685700fdcd2c5422d0 ...
✨  Done in 1.81s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: d42f41f1cfbe9347f12c2c17775e0873408f92260abb4ed943d558c73600f479 ...
✨  Done in 2.54s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Start merging your [CAT] tokens ...
Merging your [CAT] tokens in txid: 565aeec32e566931b8bdec287234bb920657f7781d48208fed964f81b0eeb5a1 ...
Minting 5.00 CAT tokens in txid: 495be2c4d1cf2cb5b1f69959e3f957d46c6638d3a8dd18739350d31df0a8d428 ...
✨  Done in 3.03s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
retry to mint token [CAT] ...
Start merging your [CAT] tokens ...
Minting 5.00 CAT tokens in txid: 1b24a75cb5696626a2e579df532cbc67778289f47d0b2f995be76deb90265d16 ...
✨  Done in 12.42s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: 26767b482434bc9bdb91c024e50264fa8bdb3952c94aa2da6c5f3a4a4d0f134f ...
✨  Done in 2.02s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: 58dc686f498bb1f42b27067547a5a57571a6568bae1479f422362b83b051bb6f ...
✨  Done in 1.82s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: 343ada5d8f0863a43e6e1f908a7769e2fcb8671057ecf24cfcf1adb38676ad22 ...
✨  Done in 1.85s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: 0db40f0315163f2704dc213d96e12505f4cda4e632be7a2641da9219f131693e ...
✨  Done in 2.44s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Start merging your [CAT] tokens ...
Merging your [CAT] tokens in txid: 62f41c073eadd1919fa0a8fac4a4d375998a80fdfc4c9f0f26532d578d805298 ...
Minting 5.00 CAT tokens in txid: 18f929ad4ae259fe81d253d7932fefbfdfb3f666755854fe238eb58060b73ce7 ...
✨  Done in 2.77s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: f8b8a2fc7c03375c0e46c4027c0b3b8c19c3ed8de6d4f037bdd41dd8178af76d ...
✨  Done in 2.01s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: 685aa88f9dba8d0e46f022c35e1867c6e4c6a52ef3d2e4315c99dc497ae7e4cf ...
✨  Done in 1.95s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: b63756e397c18d007a456de6284382cd872c4fae6cbd151b8bfdbcc42c83e056 ...
✨  Done in 1.70s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: 9a7775ca9de5f774d9c05f5f3b01a77c308273de7aaff4b1798a1a94acba4f8f ...
✨  Done in 1.90s.
yarn run v1.22.22
$ node dist/main mint -i 45ee725c2c5993b3e4d308842d87e973bf1951f5f7a804b21e4dd964ecd12d6b_0 5
Minting 5.00 CAT tokens in txid: 891a0f1673c78749665b1222cd17af681eb53b0fb4f549ba06954b227eb94b5e