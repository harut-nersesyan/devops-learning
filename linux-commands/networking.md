
# Linux Networking Commands

## 1. Ping

Check network connectivity to a remote host.

```bash
ping -c 4 example.com
```

- `ping` - Send ICMP echo requests.
- `-c 4` - Send 4 packets.
- `time` - Network latency in milliseconds.
- `packet loss` - Percentage of lost packets.

Note: Some servers block ICMP requests.

## 2. Curl

Send HTTP requests and check web server responses.

```bash
curl -I https://example.com
```

- `curl` - Transfer data using network protocols.
- `-I` - Request HTTP headers only.
- `-L` - Follow HTTP redirects.

Follow redirects:

```bash
curl -I -L https://example.com
```

Common HTTP status codes:

- `200` - OK
- `301` - Moved Permanently
- `400` - Bad Request
- `401` - Unauthorized
- `403` - Forbidden
- `404` - Not Found
- `500` - Internal Server Error
- `502` - Bad Gateway
- `503` - Service Unavailable

## 3. Nslookup

Find IP addresses associated with a domain.

```bash
nslookup example.com
```

DNS translates domain names into IP addresses.

## 4. Dig

Query DNS records.

```bash
dig example.com
```

Get a short DNS response:

```bash
dig example.com +short
```

Check mail server records:

```bash
dig google.com MX +short
```

Common DNS record types:

- `A` - IPv4 address
- `AAAA` - IPv6 address
- `CNAME` - Domain alias
- `MX` - Mail server
- `TXT` - Text records

## 5. Netstat

Display TCP connections and listening ports.

macOS example:

```bash
netstat -an -p tcp | head -20
```

Common TCP connection states:

- `LISTEN` - Waiting for incoming connections.
- `ESTABLISHED` - Active connection.
- `SYN_SENT` - Connection request sent.
- `TIME_WAIT` - Closed connection waiting for cleanup.

Note: Linux and macOS use different netstat options.

## 6. Lsof

Find processes listening on a specific TCP port.

```bash
lsof -nP -iTCP:5000 -sTCP:LISTEN
```

- `lsof` - List open files and sockets.
- `-nP` - Display numeric IP addresses and ports.
- `-iTCP:5000` - Select TCP sockets on port 5000.
- `-sTCP:LISTEN` - Show listening sockets only.

## Practical DevOps Examples

Check network connectivity:

```bash
ping -c 4 example.com
```

Check HTTP response headers:

```bash
curl -I https://example.com
```

Check DNS resolution:

```bash
dig example.com +short
```

Find the process listening on port 5000:

```bash
lsof -nP -iTCP:5000 -sTCP:LISTEN
```

These commands help DevOps engineers troubleshoot network connectivity, DNS issues, HTTP errors, and application ports.

