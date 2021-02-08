### Change snark worker fee
coda client set-snark-work-fee 0.2

### Change number of parallel snark workers (advisable to dynamically manage it using a script)
coda client set-snark-worker-parallelism 32

### To start snark worker after node starts (this might help node boot time)
coda client set-snark-worker -address $MINA_PUBLIC_KEY  

