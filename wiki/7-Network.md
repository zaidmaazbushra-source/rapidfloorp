# 7. Network Tweaks

## DNS-over-HTTPS (DoH)

Faster, private DNS resolution. Enable in Settings → Privacy & Security → DNS over HTTPS.

Recommended providers: Cloudflare (`1.1.1.1`), NextDNS.

---

## HTTP/3 & QUIC

```
network.http.http3.enabled → true
```

HTTP/3 (QUIC) reduces latency on supported sites.

---

## Parallel Connections

```
network.http.max-connections → 1800
network.http.max-persistent-connections-per-server → 10
network.http.max-urgent-start-excessive-connections-per-host → 5
```

---

## TLS Session Cache

```
network.ssl_tokens_cache_capacity → 32768
```

Larger TLS cache means less re-negotiation on return visits.

---

## Disable Speculative Loading

If you want to reduce background network traffic (useful on metered connections):

```
network.prefetch-next → false
network.predictor.enabled → false
network.http.speculative-parallel-limit → 0
```

---

## OCSP Stapling

```
security.OCSP.enabled → 0
```

Disabling OCSP reduces per-connection latency by skipping certificate revocation checks. Only do this if you have another layer of security (e.g., uBlock Origin, DNS filtering).
