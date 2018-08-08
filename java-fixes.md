# Java-Fixes.Md

----------------------------------------- 
## Error - trustAnchors parameter must be non-empty

See [This answer][trustanchor]

``` bash
# 1. Save an empty JKS file with the default 'changeit' password for Java cacerts.
#    Use 'printf' instead of 'echo' for Dockerfile RUN compatibility.
/usr/bin/printf '\xfe\xed\xfe\xed\x00\x00\x00\x02\x00\x00\x00\x00\xe2\x68\x6e\x45\xfb\x43\xdf\xa4\xd9\x92\xdd\x41\xce\xb6\xb2\x1c\x63\x30\xd7\x92' > /etc/ssl/certs/java/cacerts

# 2. Re-add all the CA certs into the previously empty file.
/var/lib/dpkg/info/ca-certificates-java.postinst configure
```

[trustachor]: https://stackoverflow.com/a/50103533/161312
-----------------------------------------
2018-06-05 17:30:16
