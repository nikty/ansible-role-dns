## dns [![Build Status](https://travis-ci.org/Oefenweb/ansible-dns.svg?branch=master)](https://travis-ci.org/Oefenweb/ansible-dns)

Set up dns in Debian-like systems.

#### Requirements

None

#### Variables

* `dns_remove_resolvconf` [default: `true`]: Whether or not to remove the `resolvconf` package
* `dns_domain` [default: `''`]: Local domain name. Most queries for names within this domain can use short names relative to the local domain
* `dns_nameservers` [default: `[8.8.8.8, 8.8.4.4]`]: Internet address(es) (in dot notation) of name servers that the resolver should query
* `dns_searches` [default: `[]`]: Search list for host-name lookup. The search list is normally determined from the local domain name; by default, it contains only the local domain name
* `dns_dhclient_rule` [default: `supersede`]: `supersede` or `prepend`, see http://manpages.ubuntu.com/manpages/precise/man5/dhclient.conf.5.html
* `dns_dhclient_file` [default: `/etc/dhcp/dhclient.conf`]: The location of the dhclient configuration file

## Dependencies

None

#### Example

```yaml
---
- hosts: all
  roles:
  - dns
```

#### License

BSD

#### Author Information

Mischa ter Smitten (based on work of jdauphant)

#### Feedback, bug-reports, requests, ...

Are [welcome](https://github.com/Oefenweb/ansible-dns/issues)!
