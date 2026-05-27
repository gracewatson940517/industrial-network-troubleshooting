# Industrial FTP Upload Troubleshooting

## Problem

Industrial PC failed to upload images to FTP server.

## Root Cause

TLS protocol mismatch or FTP configuration issue.

## Solution

Enable TLS1.2 support and verify FTP configuration.

---

# Industrial Log Troubleshooting

## Monitor Logs

```bash
tail -f /icore/eg/run/20260313-eg-main.log
```

## Filter Vehicle Logs

```bash
grep 'CAR77' /icore/eg/run/20260313-eg-main.log
```

---

# Firewall Operations

## Open Port

```bash
firewall-cmd --zone=public --add-port=9605/tcp --permanent
```

## Reload Firewall

```bash
firewall-cmd --reload
```
