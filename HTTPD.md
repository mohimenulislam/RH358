### HTTPD/Apache
**Pre-requisites:**
- Domain Registration
- Configure DNS Server ( At Least 2)
- Add A record to DNS

**WebServer**
- Package: `httpd rpm`
- Config File: `/etc/httpd/conf/httpd.conf`
- Listen: 80/tcp [if we want we can configure web server(http) in multiple port]
- Protocol: `http`/`https`
- DocumentRoot: `/var/www/html`
- DirectoryIndex: index.html
- Log:
  -  AccessLog: `/var/log/httpd/access-log`
  -  ErrorLog:  `/var/log/httpd/error-log`
- User: `apache`; Group: `apache`
- Listen: 80,81; curl http://serverip >> port 80
- http_port_t >> 80,81,443,8443
- Change Port tag: semanage port -a -t http_port_t -p tcp 8991
- File Context: httpd_sys_content_t

  

