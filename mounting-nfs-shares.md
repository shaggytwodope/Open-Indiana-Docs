# Mounting NFS shares in OpenIndiana

This tutorial assumes you already have a running NFS server.

```bash
adrian@openindiana-hipster:~$ sudo mkdir -p /media/adrian/nfs/storage # make the dir to mount the share to.
adrian@openindiana-hipster:~$ sudo chown adrian:staff -R /media/adrian # apply ownership of dirs if you want
adrian@openindiana-hipster:~$ sudo mount -F nfs 192.168.0.103:/storage /media/adrian/nfs/storage # mount the share
adrian@openindiana-hipster:~$ df -h #hold your breath!
rpool/ROOT/openindiana-1   28G  4.3G   24G  16% /
swap                      1.1G  448K  1.1G   1% /etc/svc/volatile
swap                      1.3G  129M  1.1G  11% /tmp
swap                      1.1G   76K  1.1G   1% /var/run
rpool/export               24G   19K   24G   1% /export
rpool/export/home          24G   19K   24G   1% /export/home
/export/home/adrian        24G   43M   24G   1% /home/adrian
rpool                      24G   30K   24G   1% /rpool
192.168.0.103:/storage    298G  128G  170G  43% /media/adrian/nfs/storage
adrian@openindiana-hipster:~$ ls -l /media/adrian/nfs/storage # we can see our share is mounted.
adrian@openindiana-hipster:~$ sudo umount /media/adrian/nfs/storage # unmounting is super easy!
```


[![video](http://img.youtube.com/vi/gyKhbDJk3LM/0.jpg)](https://www.youtube.com/watch?v=gyKhbDJk3LM)
