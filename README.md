# ipfw-persistent-table
 Persist the ipfw tables.

* work via console, as network connections may be lost.


## autosave on shutdown and load on startup

1. make the script runnable.
  e.g.
```
chown root    /usr/local/sbin/ipfw-persistent-table
chmod u+x,go= /usr/local/sbin/ipfw-persistent-table
```
1. add the script to firewall_coscripts in rc.conf.
 e.g.
```
firewall_coscripts="/usr/local/sbin/ipfw-persistent-table"
```

## manual load, and save.

- `/usr/local/sbin/ipfw-persistent-table save`
- `/usr/local/sbin/ipfw-persistent-table load`

## call via cron, to update current tables.

1. put the line to call this script, such as
```
*/30 * * * * root /usr/local/sbin/ipfw-persistent-table cron
```

feel free to customize it to suit your own environment.
cheers,
