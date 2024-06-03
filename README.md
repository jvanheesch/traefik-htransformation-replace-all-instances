# Reproducer for htransformation issue 72

https://github.com/tomMoulard/htransformation/issues/72 

## Problem

I am unable to replace all instances of a given string in request header.

## Steps to reproduce

- `docker compose up -d && docker compose logs --follow mitmproxy`
- `curl http://localhost -H 'Example: a input input b'`
- expected result: `mitmproxy-1 | Example: a output output b` in logs mitmproxy
- actual result: `mitmproxy-1 | Example: a input output b`
