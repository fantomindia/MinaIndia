### 1. Watch the client booting and syncing in relaxed mood

watch -n 30 "coda client status | sed -e '/ip4/d' -e '/External/d'  -e '/Configuration/d'"

### 2. Copy log files from ubuntu/liunx to windows local 

pscp.exe -P 22 -i <ppk_file_path> userid@hostname:~/.coda-config/mina-rejected-blocks.log C:\tmp


### 3. To view the transaction pool on a running node, you can use the following command (install jq:  sudo apt install jq):
coda advanced pooled-user-commands | jq . | grep fee | sort | uniq -c | sort -n


### 4. Send tokens to someone (account should be unlocked first)
coda accounts unlock -public-key $YOUR_PUBLIC_KEY

coda client send-payment \
  -amount 0.5 \
  -receiver $RECEIVER_PUBLIC_KEY \
  -fee 0.1 \
  -sender $YOUR_PUBLIC_KEY
