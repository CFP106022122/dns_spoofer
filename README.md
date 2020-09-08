# dns_spoofer

## Test on local:
```
iptables -I INPUT -j NFQUEUE --queue-num 0
iptables -I OUTPUT -j NFQUEUE --queue-num 0
python3 dns_spoof.py
```

## Test on remote:
```
iptables -I FORWARD -j NFQUEUE --queue-num 0
python3 dns_spoof.py
```
