<!-- Get NAS by pasting 2 commands to Startup Applications. Drop stuff in your Public folder, it'll be saved by your NAS--a normal computer with a normal OS, and no systemd! -->

* **Your computer**<br>
Paste this command to Startup apps, restart:<br>
`sh -c "python3 -m http.server 8000 -d ~/Public"`

* **NAS computer**<br>
Paste this command to Startup apps, replace "hostname" with the hostname of YOUR computer, restart:<br>
`sh -c "while :; do wget -m -np -N -R 'index.html*' hostname.local:8000/; sleep 10; done"`

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

WARNING: to improve privacy, use ethernet cables rather than WiFi.
Never run this or the "http.server" commands on public WiFi or on networks you don't trust!
http.server means you should NEVER use this NAS to save sensitive data, but only backups that
you wouldn't mind a judge reading through.

## Don't hack around
With physical access to someone's computer, by omitting "-d ~/Public",
you'll have access to more directories, not just "Public". That's also
accessible using the URL "hostname.local:8000". That's right. Go to your NAS
computer and try that URL in a browser, where "hostname" is the hostname
of the "Your computer".
