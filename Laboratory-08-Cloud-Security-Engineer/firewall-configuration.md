Firewall Configuration
Allow SSH
sudo ufw allow ssh

Default Deny Policy
sudo ufw default deny incoming
sudo ufw default allow outgoing

Enable Firewall
sudo ufw enable

Output
Rules updated
Rules updated (v6)
Default incoming policy changed to 'deny'
(be sure to update your rules accordingly)
Default outgoing policy changed to 'allow'
(be sure to update your rules accordingly)
Firewall is active and enabled on system startup


Allow Port 8080 (Web Application)
sudo ufw allow 8080/tcp

Output
Rule added
Rule added (v6)


Verification: sudo ufw status numbered
Status: active

     To                         Action      From
     --                         ------      ----
[ 1] 22/tcp                     ALLOW IN    Anywhere
[ 2] 8080/tcp                   ALLOW IN    Anywhere
[ 3] 22/tcp (v6)                ALLOW IN    Anywhere (v6)
[ 4] 8080/tcp (v6)              ALLOW IN    Anywhere (v6)


Verification: curl http://localhost:8080/
With port 8080 explicitly allowed, the request succeeds and returns the
default Nginx page:
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
...
<h1>Welcome to nginx!</h1>
<p>If you see this page, nginx is successfully installed and working.
Further configuration is required for the web server, reverse proxy,
API gateway, load balancer, content cache, or other features.</p>
...
</html>


What happens if ufw enable runs before ufw allow ssh?
Running sudo ufw enable before allowing SSH would immediately block all
incoming traffic, including the active SSH connection, locking the
administrator out of the server with no way back in except through the
cloud provider's emergency console.
