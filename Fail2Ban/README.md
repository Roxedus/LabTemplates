# Fail2Ban Examples

Tested on fail2ban-0.11.1-r1

Folder-structure should be drag'n'drop, you might want to change the logpaths.

## My setup

Currently deployed with the linuxserver/letsencrypt docker image, with a extra volume.

```bash
-v /mnt/user/appdata/_logs/:/f2b/:ro
```

Each container has their logfolder mapped to a subfolder in that host location. This is how I have the Gitea logs mapped.

```bash
-v /mnt/user/appdata/_logs/gitea:/data/gitea/log:rw
```

You could map the file directly, but if you can, avoid it as it breaks most logrotate implementations.
