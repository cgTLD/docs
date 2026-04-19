# cgNET

We currently use 10.0.0.0/8 (RFC1918) and fc00::/7 (IPv6 ULA).
We use 100.64.0.0/16 for internal communication between routers.
Each user gets a /16 IPv4 and a /16 IPv6

## Reserved subnets:
| Network        | Description                          |
|----------------|--------------------------------------|
| 100.64.0.0/24  | Reserved for internal usage          |
| 10.0.0.0/16    | Reserved for internal usage          |
| 10.10.0.0/16   | Exclusive for anycast networks       |
| fc00::/16      | Reserved for internal usage          |


Each router gets a /32 inside 100.64.1.0/24 where zero is replaced
with a number which also will be the second octet on your
IPv4 /16 subnet and also the numbers on your fcXX::/16 subnet, for
example: 100.64.1.45/32 would have 10.45.0.0/16 and fc45::/16.

You should not configure your router's firewall to block ICMP on
your /32.

***DNS server is 100.64.0.0***

## Current cgTLDs:
| gTLD           | Description                          |
|----------------|--------------------------------------|
| .gltd          | Not obtainable.                      |
| .fuck          | Can be obtainable at dot.fuck        |
| .linux         | Owned by @carson-coder on GitHub     |
| .unix          | Owned by @carson-coder on GitHub     |


# Root CA
root-ca.crt
```
-----BEGIN CERTIFICATE-----
MIIBrTCCAVKgAwIBAgIRAM/IlR9yTBX5p44ltIdKQYwwCgYIKoZIzj0EAwIwNDEU
MBIGA1UEChMLY2dUTEQgR3JvdXAxHDAaBgNVBAMTE2NnVExEIEdyb3VwIFJvb3Qg
Q0EwHhcNMjYwNDE5MTM1NjU4WhcNMzYwNDE2MTM1NjU4WjA0MRQwEgYDVQQKEwtj
Z1RMRCBHcm91cDEcMBoGA1UEAxMTY2dUTEQgR3JvdXAgUm9vdCBDQTBZMBMGByqG
SM49AgEGCCqGSM49AwEHA0IABLlIk5QPz+kQU5Gs5z6qzclFkJOlXiJAJoSNaRm7
KzFHoB9su+iOCABb+yB2i7Ngw6FUAb+DExMD21PSSY7HA0GjRTBDMA4GA1UdDwEB
/wQEAwIBBjASBgNVHRMBAf8ECDAGAQH/AgEBMB0GA1UdDgQWBBTueejqoMrFYK5p
ZEx/tkDL2fluNDAKBggqhkjOPQQDAgNJADBGAiEAwMMlZjaTaUGm5ZGp2rZ00hgn
SUBc2K7F4HjuZEV4cUoCIQCBEhXV1RRGFsNpI9YJiwMXak4EUng6hRGdqXkN0Usz
Rg==
-----END CERTIFICATE-----
```
