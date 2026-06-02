LAB WRITE-UP: TryHackMe Core Offensive Security

DATE: May 2026


OBJECTIVE:

The goal of this lab was to get hands-on experience with offensive security techniques, basically thinking and acting like an attacker. I wanted to understand how real hackers find weaknesses, exploit them, and gain access so l can better tighten systems defences.



TOOLS USED:

Gobuster: for directory and file brute-forcing

Kali Linux tools basic enumeration



WHAT I DID:

I started by enumerating the target website. At first, I was just blindly trying common directories, but I wasn't getting anywhere. Then I remembered Gobuster and used it with a wordlist to iterate through potential page names and directories. After a few minutes, Gobuster found several hidden pages that weren't linked anywhere. One of them led me to a login page with weak input validation. I spent way too much time trying manual guesses before realizing I could exploit a simple file upload vulnerability. I uploaded a basic webshell and boom, I had unauthorized access to the system. I was honestly surprised and a bit scared at how easy it was once I found that loophole.



KEY OBSERVATION:

Humans are still the weakest link. The developer left debug features enabled and didn't properly validate file uploads.

Gobuster is incredibly powerful for discovering hidden content that normal users would never see.

Once I was inside, privilege escalation was possible because of poor configuration.


WHAT I LEARN:

This lab really opened my eyes. Breaking in wasn't about being a genius hacker, it was about being patient, using the right tools, and taking advantage of small mistakes developers make under pressure. I now understand why proper input validation, directory listing restrictions, and regular security testing are so important. As a blue steamer, I'll be much more aware of the kind of paths attackers actually use.


CONCLUSION:

This was one of the most valuable labs I've done so far. It gave me real empathy for both sidesthe attacker's creativity and the defender's responsibility. I'm more motivated than ever to tighten defenses and think like the enemy.
