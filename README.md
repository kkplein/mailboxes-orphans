# mailboxes-orphans
script to detect dovecot mailboxes that have become 'orphaned'

The script uses the regular postfix command (postmap) to check if email boxes found under /var/vmail can still be delivered to.

When (in LDAP/AD/msql, whatever) accounts have been deleted, the mailboxes will have become an orphan.
(meaning: mails can no longer be delivered to that mailbox)

We then need to do something with that mailbox, now that it has become an orphan.

The script generates a file that you can run, to move the orphaned mailboxes to an archive location.

Later, you can permanently remove the mailboxes, or archive them.
