#### Upstart job definition for dnscrypt-proxy

Install dnscrypt-proxy: <https://github.com/opendns/dnscrypt-proxy>. Binary should be installed in ```/usr/local/sbin/dnscrypt-proxy```.

Fetch the repo:

```
$ git clone https://github.com/mkacik/upstart-dnscrypt-proxy.git
```
Distribute the files:

```
# cp upstart-dnscrypt-proxy/dnscrypt /etc/default/
# cp upstart-dnscrypt-proxy/dnscrypt.conf /etc/init/
```
Link as upstart job:

```
# ln -s /etc/init.d/dnscrypt /lib/init/upstart-job
```
Start the daemon:

```
# start dnscrypt
```

**Hint:**
If your dhclient is updating ```/etc/resolv.conf``` via dhcp, edit ```/etc/dhcp/dhclient.conf``` adding line:

```
supersede domain-name-servers 127.0.0.1;
```
Reload resolv.conf config:

```
# resolvconf -u
```
