
**Scenario:**
- Surfing the internet and the wireless connection drops off
- Wireless de-authentication
	- Denial of Service Attack

#### Main Vulnerability
----
- `802.11 management frames` sent and received by the access point
	- Used to connect device to network
	- Manage connections
	- Disconnect connections

- Earlier version, did not provide any security for the management frames
- Sent across the network without encryption
	- Susceptible to the attackers



#### Protecting against deauth Attacks
----
- IEEE has already addressed the problem with updates for the `802.11ac`
- Now some important management frames are `encrypted`
- NOT EVERYTHING is encrypted



#### Radio Frequency Jamming
---
Form of Denial of Service
- Prevent wireless communication

Transmit interfering wireless signals
- Decrease the signal-to-noise ratio at the receiving device
- Receiving device can't hear the good signal
- Sometimes unintentional



#### Wireless Jamming
---
Many different types
- Constant, random bits / Constant, legitimate frames
- Data sent at random times, hinder troubleshooting
- Reactive jamming - only when someone else tries to communicate with the access point

Needs to be somewhere close
- Difficult to be effective from a distance
- Jamming user is nearby
- `Fox Hunting` uses a directional antenna to locate where a signal might be coming from

