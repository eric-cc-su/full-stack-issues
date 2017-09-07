## **General**

### My front-end doesn't update with the latest data, UI changes, etc.

Chances are your stack simply hasn't updated/been restarted.
1. Run any preprocessors you might have. (ex. I use gulp and Sass for CSS styles `gulp styles`)
2. Restart your server (ex. `sudo service nginx restart`)
3. If you have any caching, invoke a refresh of your cache 
4. Do a hard refresh on your browser (`Cmd/Ctrl + Shift + R` for Chrome)
    - If your work depends on things like cookies, try clearing your browser data

### Browser shows "502 Bad Gateway" 

Try starting/restarting your server or any server modules you use (e.g. nginx and uwsgi).

On Unix systems you can try `sudo service nginx restart`

### Browser shows "Connection refused"

If you're running a virtual machine, check the settings to ensure that you set up port forwarding so you can access
your environment. If you're not running a virtual machine, double check your configuration to make sure that traffic
is being sent to the intended port on your localhost. (My environments typically forward to host port 8000 or 8080)

### SSH Connection Refused

1. Check your credentials: username, host, password
2. Check the port you're connecting to: `ssh user@host -p 2222` connects through port 2222
