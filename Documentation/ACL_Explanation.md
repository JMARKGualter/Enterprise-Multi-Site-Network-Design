# Access Control List (ACL) Explanation

## Overview

Access Control Lists (ACLs) are implemented to enforce the company's security policy by controlling communication between departments, branches, and external networks.

---

## ACL 101 – HR Department Isolation (HQ)

Applied on:
- HQ Router
- GigabitEthernet1/0.20 (Inbound)

Purpose:
- Prevents the HR department from accessing the Finance department.
- Prevents the HR department from accessing the Sales department.
- Allows all remaining traffic.

Security Policy:
- HR ❌ Finance
- HR ❌ Sales
- HR ✅ IT
- HR ✅ Servers
- HR ✅ Internet

---

## ACL 103 – Finance Department Isolation (HQ)

Applied on:
- HQ Router
- GigabitEthernet1/0.30 (Inbound)

Purpose:
- Prevents Finance from accessing HR.
- Prevents Finance from accessing Sales.
- Allows all remaining traffic.

Security Policy:
- Finance ❌ HR
- Finance ❌ Sales
- Finance ✅ IT
- Finance ✅ Servers
- Finance ✅ Internet

---

## ACL 104 – Sales Department Isolation (HQ)

Applied on:
- HQ Router
- GigabitEthernet1/0.40 (Inbound)

Purpose:
- Prevents Sales from accessing HR.
- Prevents Sales from accessing Finance.
- Allows all remaining traffic.

Security Policy:
- Sales ❌ HR
- Sales ❌ Finance
- Sales ✅ IT
- Sales ✅ Servers
- Sales ✅ Internet

---

## ACL 105 – Internet Protection

Applied on:
- HQ Router
- GigabitEthernet0/0 (Inbound)

Purpose:
- Blocks unsolicited traffic from the Internet from reaching the internal company network.
- Allows Internet traffic that is not destined for internal private networks.

Security Policy:
- Internet ❌ Internal VLANs
- Internal VLANs ✅ Internet

---

## ACL 106 – Batangas Branch Communication

Applied on:
- HQ Router (Serial4/0 Inbound)
- Batangas Router

Purpose:
- Allows department heads to communicate with their corresponding department heads in Headquarters.
- Allows Batangas users to access the HQ Server VLAN.
- Blocks Batangas users from accessing HQ departmental VLANs.

Allowed:
- IT Head ↔ HQ IT Head
- HR Head ↔ HQ HR Head
- Finance Head ↔ HQ Finance Head
- Sales Head ↔ HQ Sales Head
- All Batangas users → HQ Server VLAN

Blocked:
- Batangas → HQ IT Department
- Batangas → HQ HR Department
- Batangas → HQ Finance Department
- Batangas → HQ Sales Department

---

## ACL 107 – Server Access

Applied on:
- HQ Router
- GigabitEthernet2/0.100 (Outbound)

Purpose:
- Allows users from Batangas and Cebu branches to access the FTP and HTTPS services hosted on the HQ server.

Allowed Services:
- FTP (TCP Port 21)
- HTTPS (TCP Port 443)

---

## ACL 108 – Cebu Branch Communication

Applied on:
- HQ Router (Serial5/0 Inbound)
- Cebu Router

Purpose:
- Allows department heads to communicate with their corresponding department heads in Headquarters.
- Allows Cebu users to access the HQ Server VLAN.
- Blocks Cebu users from accessing HQ departmental VLANs.

Allowed:
- IT Head ↔ HQ IT Head
- HR Head ↔ HQ HR Head
- Finance Head ↔ HQ Finance Head
- Sales Head ↔ HQ Sales Head
- All Cebu users → HQ Server VLAN

Blocked:
- Cebu → HQ IT Department
- Cebu → HQ HR Department
- Cebu → HQ Finance Department
- Cebu → HQ Sales Department

---

## Branch ACLs

### ACL 110 (Batangas HR)

Blocks:
- HR → Finance
- HR → Sales

---

### ACL 111 (Batangas Finance)

Blocks:
- Finance → HR
- Finance → Sales

---

### ACL 112 (Batangas Sales)

Blocks:
- Sales → HR
- Sales → Finance

---

### ACL 120 (Cebu HR)

Blocks:
- HR → Finance
- HR → Sales

---

### ACL 121 (Cebu Finance)

Blocks:
- Finance → HR
- Finance → Sales

---

### ACL 122 (Cebu Sales)

Blocks:
- Sales → HR
- Sales → Finance