# R3con-Pipelines

# CVE-2026-87902 Timeline
| 
|
|
[CVE-2026-87902 Timeline.md](https://github.com/user-attachments/files/32928193/CVE-2026-87902.Timeline.md)

1. ## Official Patch Released

   September 22, 2026

   WordPress released version 7.1.2 to address CVE-2026-87902, a critical (CVSS 9.2) unauthenticated path traversal and local PHP file inclusion vulnerability in WordPress Core's `get_page_template()` function. Security fixes were also backported to all older maintained branches down to version 4.7.

   Source: [WordPress Security Update Advisory](https://asec.ahnlab.com/en/95580/)
2. ## First Probing Attempts

   September 22, 2026 (11:49 UTC)

   Less than five hours after the official patch became public, early internet probing and exploitation attempts were recorded. The rapid targeting highlighted how quickly threat actors can automate attacks on large attack surfaces like the WordPress ecosystem.

   Source: [Patchstack via The Next Web](https://thenextweb.com/news/wordpress-flaw-cve-2026-87902-exploited)
3. ## Official PoC Exploit Published

   September 23, 2026

   Security researcher **Robert Ressl**, who originally discovered and responsibly disclosed the vulnerability to WordPress, published the official Proof-of-Concept (PoC) exploit along with a reproducible lab environment. The PoC demonstrated how manipulating the page slug allows the template loader to reach readable PHP files outside the active theme, resulting in conditional Remote Code Execution (RCE).

   Source: [GitHub Security / Researcher PoC Repository](https://github.com/SecureWithUmer/CVE-2026-PoCs)
4. ## Mass Weaponization

   September 24, 2026

   Threat actors actively weaponized the vulnerability to bypass security boundaries, utilizing techniques like exploiting `pearcmd.php` to drop web shells into temporary directories. Multiple security vendors observed in-the-wild exploitation resulting in complete server compromise and potential data exfiltration.

   Source: Aviatrix Threat Research Center
