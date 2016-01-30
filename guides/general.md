## **General**

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
