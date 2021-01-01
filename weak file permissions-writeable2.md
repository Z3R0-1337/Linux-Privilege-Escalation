The /etc/shadow file contains user password hashes and is usually readable only by the root user.

Note that the /etc/shadow file on the VM is world-writable:

ls -l /etc/shadow

Generate a new password hash with a password of your choice:

mkpasswd -m sha-512 newpasswordhere

Edit the /etc/shadow file and replace the original root user's password hash with the one you just generated.

Switch to the root user, using the new password:

su root 