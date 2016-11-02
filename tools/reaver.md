# Reaver

Notes
-------
Reaver implements a brute force attack against Wifi Protected Setup (WPS) registrar PINs in order to recover WPA/WPA2 passphrases


Help Text
-------
```
Reaver v1.4 WiFi Protected Setup Attack Tool
Copyright (c) 2011, Tactical Network Solutions, Craig Heffner <cheffner@tacnetsol.com>

Required Arguments:
	-i, --interface=<wlan>          Name of the monitor-mode interface to use
	-b, --bssid=<mac>               BSSID of the target AP

Optional Arguments:
	-m, --mac=<mac>                 MAC of the host system
	-e, --essid=<ssid>              ESSID of the target AP
	-c, --channel=<channel>         Set the 802.11 channel for the interface (implies -f)
	-o, --out-file=<file>           Send output to a log file [stdout]
	-s, --session=<file>            Restore a previous session file
	-C, --exec=<command>            Execute the supplied command upon successful pin recovery
	-D, --daemonize                 Daemonize reaver
	-a, --auto                      Auto detect the best advanced options for the target AP
	-f, --fixed                     Disable channel hopping
	-5, --5ghz                      Use 5GHz 802.11 channels
	-v, --verbose                   Display non-critical warnings (-vv for more)
	-q, --quiet                     Only display critical messages
	-h, --help                      Show help

Advanced Options:
	-p, --pin=<wps pin>             Use the specified 4 or 8 digit WPS pin
	-d, --delay=<seconds>           Set the delay between pin attempts [1]
	-l, --lock-delay=<seconds>      Set the time to wait if the AP locks WPS pin attempts [60]
	-g, --max-attempts=<num>        Quit after num pin attempts
	-x, --fail-wait=<seconds>       Set the time to sleep after 10 unexpected failures [0]
	-r, --recurring-delay=<x:y>     Sleep for y seconds every x pin attempts
	-t, --timeout=<seconds>         Set the receive timeout period [5]
	-T, --m57-timeout=<seconds>     Set the M5/M7 timeout period [0.20]
	-A, --no-associate              Do not associate with the AP (association must be done by another application)
	-N, --no-nacks                  Do not send NACK messages when out of order packets are received
	-S, --dh-small                  Use small DH keys to improve crack speed
	-L, --ignore-locks              Ignore locked state reported by the target AP
	-E, --eap-terminate             Terminate each WPS session with an EAP FAIL packet
	-n, --nack                      Target AP always sends a NACK [Auto]
	-w, --win7                      Mimic a Windows 7 registrar [False]

Example:
	reaver -i mon0 -b 00:90:4C:C1:AC:21 -vv

```

Example Usage
-------


```
reaver -i mon0 -b bssid -vv
```

Links
-------
[Rever Google project](https://code.google.com/p/reaver-wps/)

[How to recover WPA/WPA2 passphrases](http://sviehb.files.wordpress.com/2011/12/viehboeck_wps.pdf)

[Reaver Pro](http://www.reaversystems.com/)
