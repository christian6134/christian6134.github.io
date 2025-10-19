
**Capture Filters**: Used for "capturing" only the packets valid for the used filter
**Display Filters**: Used for "viewing" packets valid for the used filter

**Filters**: Specific queries designed for protocols
"If you can click on it, you can filter and copy it"


**Apply As Filter**
Most basic way of filtering traffic
While investigating a capture file
- Click on field you want to filter
- Right click / Analyze -> Filter


**Conversation Filter**
Apply as Filter only filters a single entity of the packet

**Scenario**: You want to investigate a specific packet number and all linked packets by focusing on IP addresses and Port Numbers
- Conversation Filter helps view only related packets
- Analyze -> Conversation Filter


**Colorize Conversation**
- Highlights linked packets without apply a display filter
- Doesn't reduce the number of packets displayed
- Colorizes select linked packets within the Packet View


**Prepare as Filter**
- Helps create display filters using the right click menu
- Does apply filters after choice
- Adds required query to pane and waits for execution command 
- Or another chosen filtering option "..and/or.."


**Apply as Column**
- Add columns to the list pane
- Click on a value and apply it to the column


**Follow TCP Stream**
- Chance to see unencrypted data
- Streams are shown in blue (server stream) and red (client stream)


**Exercise**
- filter pane, filter query
- no. of displayed packets
- follow http stream, filter for "artists"