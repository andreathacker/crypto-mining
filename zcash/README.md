# ZCash Miner Setup

https://blockoperations.com/zcash-miner-ubuntu-linux-16-04-optiminer-1-5-amd-gpus/

https://zec.nanopool.org/help

EWBF Linux CUDA

```
# Reduce power level of GPU 0 to 90W
sudo nvidia-smi -i 0 -pl 90

tmux new-session -d -s mining
tmux send-keys -t mining "COMMAND SCRIPT" C-m
```
