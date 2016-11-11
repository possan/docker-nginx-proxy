NGINX-Proxy
===========

Proxies linked containers behind a single endpoint, Optionally terminates SSL on multiple domains


Configuration
-------------

Environment variables:

On the proxy service:

* `[id]_SERVER_CRT` Your server certificates.
* `[id]_SERVER_KEY` Your private key.
* `[id]_SERVER_DOMAIN` Domain name(s) for certificate, comma separated if multiple, use `.example.tld` for wildcards.

For each linked container:

* `VIRTUAL_HOST` Domain(s) for linked container, comma separated if multiple.

Note that certificates and keys both have newlines in them, if you're having trouble specifying new lines on Docker Cloud for example, you can substitute all new lines for `\n`.
