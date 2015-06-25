#DuckDNS

Run the DuckDNS updater for dynamic DNS in a container

##Install On unRaid:

On unRaid, install from the Community Repositories and enter the app folder location.


##Install On Other Platforms (like Ubuntu, Synology 5.2 DSM, etc.):

On other platforms, you can run this docker with the following command:

```
docker run -d --name="Duckdns" -e SUBDOMAIN="XXXX" -e TOKEN="YYYY" -v /path/to/config:/config:rw -v /etc/localtime:/etc/localtime:ro aptalca/docker-duckdns
```

###Setup Instructions
- Replace the variable "/path/to/config" with your choice of folder on your system. That is where the config files will reside, and they will survive an update, reinstallation, etc. of the container.
- Visit http://www.duckdns.org to register your subdomain
- Replace XXXX with your DuckDNS subdomain
- Replace YYYY with your DuckDNS token
- Start the container
- Check the log file 5 minutes later to make sure it is working correctly
