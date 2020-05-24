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
