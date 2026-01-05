
## Task 1: Design Security Group Rules

| Rule | Type | Protocol | Port | Source       | Purpose      |
|------|------|----------|------|--------------|--------------|
| 1    | SSH  | TCP      | 22   | My Public IP | Admin access |
| 2    | HTTP | TCP      | 80   | 0.0.0.0/0    | Web traffic  |
| 3    | HTTPS| TCP      | 443  | 0.0.0.0/0    | Secure web   |
| 4    | Custom TCP | TCP | 8080 | 10.0.0.0/8 | Internal API |

## Task 5: Troubleshooting Exercise

| Symptom | Likely Cause | Solution |
|---------|--------------|----------|
| Can't SSH to instance | Missing SSH rule or incorrect Source IP. | Add inbound rule for Port 22 (SSH) with your public IP as source. |
| Website not loading | Missing HTTP/HTTPS rules. | Add inbound rules for Port 80 (HTTP) and 443 (HTTPS) from 0.0.0.0/0. |
| API calls timing out | Missing Custom TCP rule for port 8080 or incorrect source CIDR. | Verify and add inbound rule for Port 8080 from the specific internal network CIDR (e.g., 10.0.0.0/8). |
