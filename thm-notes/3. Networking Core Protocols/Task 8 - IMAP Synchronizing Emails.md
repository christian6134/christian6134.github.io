
What if you want to check your email **from your office desktop computer and from your laptop or smartphone?** In this scenario, you need a protocol that allows synchronization of messages instead of deleting a message after retrieving it. One solution to maintaining a synchronized mailbox across multiple devices is **Internet Message Access Protocol (IMAP).**


**Internet Message Access Protocol**
-------------
- Synchronizes **read, moved and deleted messages**
- **POP3:** Minimizes use of server storage as messages are **downloaded** and then **deleted**
- **IMAP**: Requires more server storage as it needs to store for synchronized copies


**SOME IMAP Commands**
-----------------------
- `LOGIN <username> <password>` authenticates the user
- `SELECT <mailbox>` selects the mailbox folder to work with
- `FETCH <mail_number> <data_item_name>` Example `fetch 3 body[]` to fetch message number 3, header and body.
- `MOVE <sequence_set> <mailbox>` moves the specified messages to another mailbox
- `COPY <sequence_set> <data_item_name>` copies the specified messages to another mailbox
- `LOGOUT` logs out


`Uses TCP Port 143 by Default`


![[Screenshot 2025-06-26 at 11.12.11 AM.png]]

