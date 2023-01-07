# glFTPd-v2.13-STABLE

```
Change: its now possible to use bouncer IDNT with ipv6 even without providng DNS hostname. The IDNT line would be "IDNT <ident>@<ipv6_ip_address>:<DNS hostname or empty string>".
	Since ipv6 ip contains ':' its important to add one at the end to denote the DNS hostname start (which can be empty).
New:	Added 'nonumdir <path>' config option to disable the "CWD <number>" feature in certain paths. It normally jumps to <number>-newest directory but its not useful for everyone.
New:	Added 'ignore_recursive_dirlist [0/1]' option to ignore the recursive directory listion option (like 'STAT -R') as it can be quite resource heavy.
Fix:	Fixed dirlog cache update when the dirlog is full and a new entry needs to be added. This can have quite huge influence on dirlog performance.
New:	Added option '-m' for glftpd to switch xferlog time logging from seconds to miliseconds.
Fix:	Fix external tools (gl_spy, etc) to understand keyword size of 30 charts like glftpd.
New:	"botscript_all_characters 1" glftpd.conf option allow all characters to be passed to botscript.
Change:	Changed the default cipher list for non TLS1.3 connections to 'HIGH+EECDH+TLSv1.2:HIGH+EDH+TLSv1.2:!aNULL:!MD5' to allow glftpd to fxp with servers that have DSA certificate still.
Change:	Xferlog will now replace invalid characters in a filename with a '?' for both upload and download.
Fix:	Allow SITE TAKE/GIVE <credits> command to accept ammount specified by more then 10 characters.
New:    SITE CHPASS now logs password changes to sysop.log.
New:    The CERT_FILE config option now automatically loads the whole certificate chain from the
        PEM file.
New:    Added a new KEY_FILE config option so you can specify a separate PEM file with your private
        key.
New:    It is now possible to specify for which path or permissions the conversion of "dir_names" and "file_names" should apply. The argument "-" inside the conversion rule
	is followed by the directory wildcard and permissions arguments.
```
