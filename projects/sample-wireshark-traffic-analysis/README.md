# Sample: Wireshark Network Traffic Analysis (Template Walkthrough)

**Summary:** Investigated suspicious outbound traffic; identified periodic DNS beacons; recommended egress filtering + DNS logging.

## Steps
1. Captured traffic in a safe lab using sample PCAP (no production data).
2. Applied display filters to isolate DNS and HTTP anomalies.
3. Mapped domains to reputational sources (document method, not raw keys).

## Findings (Example)
- Repeating DNS queries every 60s to `example-bad-domain[.]com` → likely beaconing.
- Host `lab-win10` initiated traffic; user `testuser` logged in at time T.

## Recommendations
- Block domain at DNS resolver.
- Add detection for periodic DNS queries >N/min.
- Educate users on phishing indicators.

> Replace this entire file with your real (non-sensitive) analysis when ready.
