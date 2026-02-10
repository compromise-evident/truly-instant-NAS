<!-- Get NAS by pasting 1 command to Startup Applications. Drop stuff in your Public folder, it'll be saved by your NAS--a normal computer with a normal OS, and no systemd! -->

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

WARNING:
To improve privacy, use ethernet cables rather than WiFi.
Never run this or the "http.server" commands on public WiFi or on networks you don't trust!
http.server means you should NEVER use this NAS to save sensitive data, but only backups that
you wouldn't mind a judge reading through.
