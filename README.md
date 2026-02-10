<!-- Get NAS by pasting 2 commands to Startup Applications. Runs in background. Drop stuff in your Public folder, it'll be saved by your NAS--another normal computer with a normal OS. No systemd. -->

* **Your computer**<br>
Paste this command to Startup apps, restart:<br>
```
sh -c "python3 -m http.server 8000 -d ~/Public"
```

* **NAS computer**<br>
Paste this command to Startup apps, replace "hostname" with the hostname of YOUR computer, restart:<br>
```
sh -c "while :; do wget -m -np -N -R 'index.html*' hostname.local:8000/; sleep 10; done"
```
