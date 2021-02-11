### Watch the client booting and syncing in relaxed mood

watch -n 30 "coda client status | sed -e '/ip4/d' -e '/External/d'  -e '/Configuration/d'"
