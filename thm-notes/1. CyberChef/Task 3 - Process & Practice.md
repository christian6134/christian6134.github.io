
![[CyberChef-process.png]]
## Extractors
-----
The specific operations mentioned in the table below fall under the **Extractors** category.

|Specific|Description|
|---|---|
|Extract IP addresses|Extracts all IPv4 and IPv6 addresses.|
|Extract URLs|Extracts Uniform Resource Locators (URLs) from the input. The protocol (HTTP, FTP, etc.) is required, otherwise there will be far too many false positives.|
|Extract email addresses|Extracts all email addresses from the input.|

The `Extract IP addresses` will extract any valid IPv4/6 address from any given input. We recommend checking our existing room for a quick recap of networking: [Networking Concepts](https://tryhackme.com/r/room/networkingconcepts)

The `Extract email addresses` extracts any strings and characters with this format, anything@domain[.]com. Examples of domains include **hotmail.com**, **google.com**, **tryhackme.com**, and **yahoo.com**

`Extract URLs` extracts Uniform Resource Locator, commonly known as URL. , a URL is the address used to access resources on the internet. You can check the [Web Applications Basics](https://tryhackme.com/r/room/webapplicationbasics) room if you would like to dig deeper into URLs and web applications.

## Date and Time
----
The specific operations in the table below fall under the **Date / Time** category.

|Specific|Description|
|---|---|
|From UNIX Timestamp|Converts a UNIX timestamp to a datetime string.|
|To UNIX Timestamp|Parses a datetime string in UTC and returns the corresponding UNIX timestamp.|

A UNIX timestamp is a 32-bit value representing the number of seconds since January 1, 1970 UTC (the UNIX epoch). To convert "**Fri Sep 6 20:30:22 +04 2024**" into a UNIX Timestamp, use the operations `To UNIX Timestamp`, where the result would be `1725654622`. If you wish to convert it back to a more readable format, you can use `From UNIX Timestamp`.

## Data Format
-----
The specific operations in the table below fall under the **Data format** category.

|Operations|Description|Examples|
|---|---|---|
|From Base64|This operation decodes data from an ASCII Base64 string back into its raw format.|`V2VsY29tZSB0byB0cnloYWNrbWUh` becomes `Welcome to tryhackme!`|
|URL Decode|Converts URI/URL percent-encoded characters back to their raw values.|`https%3A%2F%2Fgchq%2Egithub%2Eio%2FCyberChef%2F` becomes `https://gchq.github.io/CyberChef/`|
|From Base85|notation for encoding arbitrary byte data. It is usually more efficient than Base64. This operation decodes data from an ASCII string (with an alphabet of your choosing, presets included).|`BOu!rD]j7BEbo7` becomes `hello world`|
|From Base58|is a notation for encoding arbitrary byte data. It differs from Base64 by removing efficiently misread characters (i.e. l, I, 0, and O) to improve human readability.|`AXLU7qR` becomes`Thm58`|
|To Base62|is a notation for encoding arbitrary byte data using a restricted set of symbols that humans can conveniently use and process by computers. The high number base results in shorter strings than with the decimal or hexadecimal system|`Thm62` becomes`6NiRkOY`|

Operations such as `Base(64, 85, 58, 62)` are known as **base encodings**. Base encoding takes binary data (strings of 0s and 1s) and transforms it into a text-based representation using a specific set of ASCII (American Standard Code for Information Interchange) characters.

Although we have a dedicated room for [Hashing Basics](https://tryhackme.com/r/room/hashingbasics), let's have a quick overview and discuss the most commonly used operation, `Base64`.

Our example would be to encode the letters "**THM**". We have a short ASCII Table here that we can use for reference. If you want to view the complete ASCII Table, please refer to this page [here](https://en.wikipedia.org/wiki/ASCII).

|Decimal|Binary|Symbol|-|Decimal|Binary|Symbol|
|---|---|---|---|---|---|---|
|65|01000001|A||78|01001110|N|
|66|01000010|B||79|01001111|O|
|67|01000011|C||80|01010000|P|
|68|01000100|D||81|01010001|Q|
|69|01000101|E||82|01010010|R|
|70|01000110|F||83|01010011|S|
|71|01000111|G||84|01010100|T|
|72|01001000|H||85|01010101|U|
|73|01001001|I||86|01010110|V|
|74|01001010|J||87|01010111|W|
|75|01001011|K||88|01011000|X|
|76|01001100|L||89|01011001|Y|
|77|01001101|M||90|01011010|Z|

  

## Step 1: Convert To Binary and Merge(Manually)

Based on our table above, **T = 01010100**, **H=01001000**, **M = 01001101**. Next, concatenate these binaries and make sure they have 24 characters. You should have `010101000100100001001101`

## Step 2: Divide and Convert to Decimal(Manually)

Separate `010101000100100001001101` into 6 characters each. You should have `010101` `000100` `100001` `001101`. These are 6-bit characters; we should have four instances of this now. We need to convert each instance to Decimal. Let's convert, then!

|Binary|Decimal (Base10)|
|---|---|
|010101|21|
|000100|4|
|100001|33|
|001101|13|

  

## Step 3: Convert to Base64 (Manually)

Now that we have the Numbers from the previous step, which are `21`, `4`, `33`, and `13`, let's look for the equivalent characters from our table below. This table represents a base64 index table.

|Index|Character|-|Index|Character|-|Index|Character|
|---|---|---|---|---|---|---|---|
|0|**A**||26|**a**||52|**0**|
|1|**B**||27|**b**||53|**1**|
|2|**C**||28|**c**||54|**2**|
|3|**D**||29|**d**||55|**3**|
|4|**E**||30|**e**||56|**4**|
|5|**F**||31|**f**||57|**5**|
|6|**G**||32|**g**||58|**6**|
|7|**H**||33|**h**||59|**7**|
|8|**I**||34|**i**||60|**8**|
|9|**J**||35|**j**||61|**9**|
|10|**K**||36|**k**||62|**+**|
|11|**L**||37|**l**||63|**/**|
|12|**M**||38|**m**||||
|13|**N**||39|**n**||||
|14|**O**||40|**o**||||
|15|**P**||41|**p**||||
|16|**Q**||42|**q**||||
|17|**R**||43|**r**||||
|18|**S**||44|**s**||||
|19|**T**||45|**t**||||
|20|**U**||46|**u**||||
|21|**V**||47|**v**||||
|22|**W**||48|**w**||||
|23|**X**||49|**x**||||
|24|**Y**||50|**y**||||
|25|**Z**||51|**z**||||

Upon checking from the table, we should have found its corresponding character by now. 

|Index|Characters|
|---|---|
|21|V|
|4|E|
|33|h|
|13|N|

Combine these characters, and you should have the equivalent of "THM" in base64 format. The answer would be `VEhN`.

Woah! Isn't that amazing? You just converted a set of characters into base64 manually.

Now, let’s discuss the `URL Decode`. This works by converting the percent-encoded characters back to their raw values. For a reference of these values, you can check the page [here](https://en.wikipedia.org/wiki/Percent-encoding). Note that the default character set in HTML5 is **UTF-8**. Check the table below for a quick overview of what we can typically see in a URL.

|Characters|From UTF-8|
|---|---|
|:|%3A|
|/|%2F|
|.|%2E|
|=|%3D|
|#|%23|



### EXERCISE
-----
`What is the hidden email address?
- Paste or upload the input file
- Select `Extract Email Addresses`


`What is the hidden IP address that ends in .232?
- `Extract all IPs`


`What is the binary value of the decimal number 78?  
- `From Decimal`
- `To Binary`


`What is the URL encoded value of `https://tryhackme.com/r/careers`?
- `URL Encoded`
- `Encode all Special Characters`
