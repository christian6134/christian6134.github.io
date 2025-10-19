
### What is BAC?
---------
- When a regular visitor is able to access **protected pages**
	- Being able to view sensitive information from other users (Like Private Youtube Videos)
	- Accessing unauthorized functionality

- Broken Access Control allows attackers to bypass authorization, allowing them to view sensitive data. 

#Example
For example, a [vulnerability was found in 2019](https://bugs.xdavidhu.me/google/2021/01/11/stealing-your-private-videos-one-frame-at-a-time/), where an attacker could get any single frame from a Youtube video marked as private. The researcher who found the vulnerability showed that he could ask for several frames and somewhat reconstruct the video. Since the expectation from a user when marking a video as private would be that nobody had access to it, this was indeed accepted as a broken access control vulnerability.

