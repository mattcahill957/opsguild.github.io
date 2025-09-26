---
layout: default
title: "Following the Script: My First Phishing Incident Response Using a SOC Playbook 📄"
date: 2025-09-25
---

<!-- Post Title Banner -->
<div style="background-color: #000; color: #fff; padding: 60px 20px; text-align: center;">
  <h1 style="margin: 0; font-size: 3rem;">Following the Script: My First Phishing Incident Response Using a SOC Playbook 📄</h1>
  <p style="margin-top: 10px; color: #ccc; font-size: 1rem;">Sepetember 2025</p>
</div>

<!-- Post Content -->
<div style="max-width: 800px; margin: 40px auto; line-height: 1.7; font-size: 1.1rem; padding: 0 20px;">

<p>In cybersecurity, quick action is vital, but coordinated action is non-negotiable. As an aspiring analyst, I recently got hands-on with a Security Operations Center (SOC) playbook to manage a critical phishing incident. This project demonstrated my ability to follow established, professional procedure under pressure—a core skill for any incident responder.</p>

<h2>1. The Problem: A Malicious File Hash 🚨</h2>

<p>The scenario placed me as a Level-One SOC Analyst at a financial services company.</p>

<p>The incident began with a high-priority security alert: a suspicious file had been downloaded to an employee's computer, originating from a phishing email. The key piece of initial information was that the file's SHA256 hash had already been verified as malicious in a previous investigation. This immediately validated the threat, turning a suspicious alert into a confirmed, critical incident.</p>

<p>My task was clear: follow the organization's specific Phishing Playbook to investigate, contain the threat, and formally resolve the alert ticket, all while documenting my actions in an Incident Handler's Journal.</p>

<h2>2. My Process: Navigating the Phishing Playbook</h2>

<p>Playbooks are essential because they ensure every analyst follows the same, proven steps, minimizing the impact of an incident and reducing response time. My response was guided by the Playbook's critical phases: Triage, Validation, Containment, Eradication, and Resolution.</p>

<h2>Phase 1: Validation and Triage</h2>

<p>Since the threat was pre-validated by the malicious file hash, my triage phase was focused and immediate. The playbook guided me to confirm that the file's presence on the endpoint represented an active compromise. There was no need to waste time investigating if the file was truly benign; the focus immediately shifted to containment.</p>

<h2>Phase 2: Containment and Eradication</h2>

<p>This was the most critical action phase. The playbook directed specific, step-by-step measures to isolate the threat and prevent any further damage or lateral movement across the network.</p>

<p>-Containment Action: The first priority was to isolate the infected endpoint (the employee's machine) from the rest of the corporate network. This action, often performed in coordination with a network team, is crucial to prevent the malware from spreading, connecting to a Command and Control (C2) server, or attempting to steal credentials.</p>

<p>-Eradication Action: Following isolation, the playbook mandated the complete removal of the malicious file, typically by deleting or quarantining it based on its confirmed SHA256 hash.</p>

<h2>Phase 3: Resolution and Documentation</h2>

<p>After taking containment and eradication steps, I moved to the final phase of updating the incident record. The process required a detailed update of the official Alert Ticket.</p>

<h2>3. The Outcome: Finalizing the Alert Ticket ✅</h2>

<p>Completing the alert ticket demonstrates not only technical skill but also clear, professional communication.</p>

<p>-Updated Ticket Status: I set the status to "Resolved – Escalated for L2." This is a deliberate choice: while the immediate containment steps were complete as per the Level-One analyst's playbook, the incident required escalation to a Level 2 (L2) analyst for a full forensic analysis.</p>

<p>-Ticket Comments/Findings: I provided a concise summary of the incident and the justification for my actions:
  -Description: "Phishing alert validated; SHA256 file hash confirmed malicious, leading to immediate compromise of an internal endpoint."
  -Reasoning for Escalation: "The incident was successfully contained by isolating the endpoint as per the playbook. It is now escalated to Level 2 for full forensic analysis to determine the scope of the breach, check for persistence mechanisms, and establish if any data exfiltration or privilege escalation occurred."</p>

<p>This lab was an invaluable exercise in structured incident management. It gave me hands-on experience in process adherence, threat validation, and professional documentation, reinforcing my ability to be a reliable and disciplined component of any security team.</p>

<h2>—Matt</h2>

</div>
