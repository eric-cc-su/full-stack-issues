# **NGINX**

## Cached Static Files Issues

This is in the case that either old versions of files are being served or static files are cut off.

I've had an issue where some of my javascript files are not only old, but the rest of the file had
been severed. This can be fixed by changing your nginx configuration, especially if you are running
on a virtual machine.

In your nginx.conf (`/etc/nginx/nginx.conf`), set "sendfile" to off, or remove the line entirely.