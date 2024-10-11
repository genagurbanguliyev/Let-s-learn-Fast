---
Technology: system_ubuntu
tags:
  - bash
  - "#server"
  - share
created_at: 2024-09-26
---
### Working with share files
send file from local computer to server
```
scp /path/to/local/file username@remote_host:/path/to/remote/directory
```


Here the `remote` can be a FQDN or an IP address.
On the other hand if you are on the computer wanting to receive file from a remote computer:

```
scp username@remote:/file/to/send /where/to/put
```

`scp` can also send files between two remote hosts:

```
scp username@remote_1:/file/to/send username@remote_2:/where/to/put
```

So the basic syntax is:

```
scp username@source:/location/to/file username@destination:/where/to/put
```

You can read [`man scp`](http://linux.die.net/man/1/scp) to get more ideas on this.