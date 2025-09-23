---
layout: default
title: "From Alert to Action: Responding to a DoS Attack in a Simulated Lab 💥"
date: 2025-09-23
---

<!-- Post Title Banner -->
<div style="background-color: #000; color: #fff; padding: 60px 20px; text-align: center;">
  <h1 style="margin: 0; font-size: 3rem;">From Alert to Action: Responding to a DoS Attack in a Simulated Lab 💥</h1>
  <p style="margin-top: 10px; color: #ccc; font-size: 1rem;">Sepetember 2025</p>
</div>

<!-- Post Content -->
<div style="max-width: 800px; margin: 40px auto; line-height: 1.7; font-size: 1.1rem; padding: 0 20px;">

<p>An automated alert. A connection timeout error. A flood of suspicious network traffic overwhelming a critical web server. This was the challenging scenario I recently faced in a lab that put my skills to the test as a security analyst. This project allowed me to step into the shoes of an incident responder, from identifying an active attack to implementing initial containment measures and understanding its business impact.</p>

<h2>1. The Problem: A Website Under Attack 🕵️</h2>

<p>The scenario began with me working as a security analyst for a travel agency. The company’s website is vital for advertising sales and promotions, serving both customers and internal employees who search for vacation packages.</p>

<p>One afternoon, an automated alert flashed across my monitoring system, indicating a serious problem with the web server. My immediate action was to verify the issue firsthand. Attempting to visit the company’s website, I was met with the dreaded "connection timeout" error message in my browser. The site was down, and the clock was ticking.</p>

<p>To get a clearer picture of what was happening, I immediately deployed a packet sniffer to capture data in transit to and from the web server. What I observed was alarming: a massive and abnormal volume of TCP SYN requests flooding in, all originating from an unfamiliar IP address. The web server was clearly overwhelmed, struggling to respond to this deluge of incoming traffic, and rapidly losing its ability to function. It was evident the server was under a coordinated attack.</p>

<h2>2. My Process: From Triage to Containment 🛑</h2>

<p>Based on the overwhelming evidence, I quickly identified the attack as a SYN flood. This is a classic form of Denial-of-Service (DoS) attack that exploits a fundamental part of how networks establish connections: the TCP three-way handshake.</p>

<p>Here’s how a SYN flood works:</p>

<p>1. Normally, a client sends a SYN (synchronize) packet to initiate a connection.</p>

<p>2. The server responds with a SYN-ACK (synchronize-acknowledge) packet.</p>

<p>3. The client then completes the handshake with an ACK (acknowledge) packet.</p>

<p>In a SYN flood, a malicious actor sends a huge number of SYN requests but either uses a spoofed (fake) source IP address or simply never sends the final ACK packet. This leaves the server with countless "half-open" connections, consuming its memory and processing power as it waits for a response that will never come. Eventually, the server exhausts its resources and can no longer establish legitimate connections.</p>

<p>My immediate response involved two critical steps for containment:</p>

<p>1. Server Offline: To prevent further resource exhaustion and allow the server to recover from the overload, I temporarily took the web server offline. This was a necessary step to stabilize the system.</p>

<p>2. Firewall Block: I configured the company's firewall to block the specific malicious IP address that was sending the abnormal number of SYN requests.</p>

<p>It was crucial to recognize, however, that simply blocking a single IP address is often a temporary solution at best. Attackers can easily spoof other IP addresses or leverage a botnet (creating a Distributed Denial-of-Service or DDoS attack) to circumvent such basic blocks. This highlighted the need for a more robust, long-term strategy.</p>

<h2>3. The Outcome: Understanding the Impact and Future Steps 💡</h2>

<p>The SYN flood attack had a significant negative impact on both the travel agency's network performance and its business operations:</p>

<p>-Network Performance: The most direct effect was the denial of service. The server's resources (CPU, memory, network bandwidth) were completely consumed by the flood of malicious requests, rendering it unresponsive to legitimate users. This manifested as the "connection timeout" errors experienced by both employees and customers.</p>

<p>-Business Operations: For a travel agency, an offline website is a direct hit to the bottom line. With the website down, customers couldn't browse vacation packages or make bookings, leading to immediate lost sales and revenue. Beyond the financial impact, such an incident can severely damage the company's reputation and erode customer trust.</p>

<p>Following this initial containment, my next immediate step would be to alert my manager. I would provide a concise incident report outlining the type of attack, its impact, and the temporary measures taken. We would then discuss next steps, which would likely include:</p>

<p>-Implementing advanced DDoS mitigation services.</p>

<p>-Configuring the firewall with more sophisticated rate-limiting rules to prevent a single source from overwhelming the server.</p>

<p>-Enhancing monitoring and alerting to detect such attacks more rapidly.</p>

<p>This simulated incident was an invaluable learning experience. It provided hands-on practice in threat identification, incident triage, and implementing initial containment measures, all of which are essential skills for an aspiring security analyst. It reinforced the importance of quick, decisive action and the need for a layered security approach to protect critical assets from ever-evolving threats.</p>

<p>I hope this walkthrough shed some light on the dynamics of a DoS attack and incident response. I have some more content coming up so stay tuned!</p>

<h2>—Matt</h2>

</div>
