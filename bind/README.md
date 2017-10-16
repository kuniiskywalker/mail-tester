Build
```
sudo make build
```

Generate rndc.key
```
sudo make keygen
```

Run
```
sudo make run
```

Forward DNS
```
nslookup fish.kunii.local {docker vm ip}
```

Forward MX
```
nslookup -type=mx kunii.local 127.0.0.1
```

