Upstart job definition for dnscrypt-proxy

1. Install dnscrypt-proxy: <https://github.com/opendns/dnscrypt-proxy>. Binary should be installed in ```/usr/local/sbin/dnscrypt-proxy```
2. Fetch files

```
$ git clone https://github.com/mkacik/upstart-dnscrypt-proxy.git 

```
3. Distribute the files

```
# cp upstart-dnscrypt-proxy/dnscrypt /etc/default/
# cp upstart-dnscrypt-proxy/dnscrypt.conf /etc/init/
```
4. Link as upstart job

```
# ln -s /etc/init.d/dnscrypt /lib/init/upstart-job
```
5. Start the daemon

```
# start dnscrypt
```
