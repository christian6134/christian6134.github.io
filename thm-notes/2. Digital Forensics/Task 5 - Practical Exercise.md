
*We have been given evidence that we must analyze using various tools*
- `pdfinfo`
- `exiftool`

**Context:**
- When you create a text file, metadata gets saved by the operating system
- File creation date, last modification date.

*What does pdfinfo do?*
- Reads the metadata info
- Displays PDF titles, subject, author, creator date

*What is EXIF?*
- Exchangeable Image File Format
- Standard for saving metadata of an image

Camera model / Smartphone model
Date and Time of image capture
Photo settings



`pdfinfo ransom-letter.pdf`
- Displays pdf metadata
- **What is the authors name?**
	- `pdfinfo ransom-letter.pdf | grep Author`
	- **Ann Gree Shepherd**

`exiftool letter-image.jpg | grep GPS`
- Plug in coordinates to find a street name
- **Milk Street**

`exiftool letter-image.jpg | grep Camera`
- **Canon EOS R6**

