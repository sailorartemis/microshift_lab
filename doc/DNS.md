## DNS

A Wildcard DNS Entry is needed for the Microshift Cluster.  
The are Multieple sulotions:

### Local DNS
- Set static wildcard DNS entry on your DNS Server for your Microshift Cluster. U could set it in Adguard, Pi-hole or other DNS Server.

### Hosts Entry
- Set multible static DNS entry via hosts
Linux:
```bash
/etc/hosts
```

Windows:
```bash
C:\Windows\system32\drivers\etc\hosts
```

### Public wildcard DNS
- Use a free wildcard DNS service:
https://nip.io/

