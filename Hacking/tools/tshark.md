#network #enumeration 

TShark is a terminal oriented version of Wireshark designed for capturing and displaying packets when an interactive user interface isn’t necessary or available. It supports the same options as wireshark. For more information on tshark consult your local manual page (man tshark)

```bash
tshark -r <file.pcap>
```

```bash
#show only http traffic
tshark -r <file.pcap> -Y 'http'
```

```bash
tshark -r <file.pcap> -Y "ip.src==192.168.252.128 && ip.dst==42.56.23.1"
```

```bash
tshark -r <file.pcap> -Y "http.request.method==GET"
```

Only show WiFi traffic
```bash
tshark -r <file.pcap> -Y 'wlan'
```

View the deauthentication packets
```bash
tshark -Y 'wlan.fc.type_subtype==0x000c'
```

Display WPA handshake packets
```bash
tshark -Y 'eapol'
```

Print SSID and BSSID values for all beacon frames
```bash
tshark -Y "wlan.fc.type_subtype==8" -Tfields -e wlan.ssid -e wlan.bssid
```