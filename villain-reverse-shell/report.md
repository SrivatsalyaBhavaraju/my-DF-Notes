# Reverse Shell (Villain) — Lab Report

> **Legal & Ethical Notice:** This exercise must be performed **only** on systems you own or have explicit written permission to test, and strictly inside an isolated lab (VMs, host-only networks). No production networks. Document consent if applicable.

## 🧭 Lab Overview
- **Goal:** Understand C2/reverse-shell concepts and blue-team detections in a safe lab.
- **Tools:** Villain (C2 framework), Python 3, Kali/Ubuntu attacker VM, Windows/Linux victim VM.
- **Network:** Host-only/isolated; snapshots taken before starting.

## 🧪 Environment
- **Attacker VM:** _OS/Version/IP_ (lab-only)
- **Victim VM:** _OS/Version/IP_ (lab-only)
- **Hardening/EDR present?:** _value_
- **Time of test:** _value_

## 🔄 High-Level Procedure (no weaponization details)
1. Start the C2/listener in the attacker VM.
2. Prepare a benign, lab-only payload and document its settings (no live targets, sanitize addresses).
3. Execute the payload inside the victim VM only.
4. Verify a session was established; capture minimal, non-sensitive screenshots.
5. Observe blue-team signals (AV/EDR alerts, Windows/Sysmon events, network logs).

## 🧰 Detection & Defense Notes
- **Host Indicators:** _e.g., process tree, parent-child anomalies, command-line args_.
- **Windows/Sysmon Events:** _e.g., 1 (Process Create), 3 (Network), 10 (Process Access)_.
- **Network Indicators:** _e.g., unusual outbound connections, DNS_.
- **Mitigations:** _e.g., application control, firewall egress rules, EDR policies_.

## 🧠 Inference
_Short takeaways on risks, detection opportunities, and controls._

## 🖼️ Screenshots
> Add only lab screenshots (redact hostnames/IPs if needed):
>
> ![C2 console (lab)](screenshots/c2-console.png)
> ![Detection alert](screenshots/defender-alert.png)

## 🧹 Cleanup
- Revert snapshots; verify no persistence remains; document restoration.
