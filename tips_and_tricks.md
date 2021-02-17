### Watch the client booting and syncing in relaxed mood

watch -n 30 "coda client status | sed -e '/ip4/d' -e '/External/d'  -e '/Configuration/d'"

### Copy log files from ubuntu/liunx to windows local 

pscp.exe -P 22 -i <ppk_file_path> userid@hostname:~/.coda-config/mina-rejected-blocks.log C:\tmp


### To view the transaction pool on a running node, you can use the following command (you will need to install jq, which is used to format the output of the following command, e.g., sudo apt install jq):
coda advanced pooled-user-commands | jq . | grep fee | sort | uniq -c | sort -n

