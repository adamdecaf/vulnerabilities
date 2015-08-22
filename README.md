**fuzzdb**: Web Fuzzing Discovery and Attack Pattern Database

#### Notice

This project seems to have been fairly abandoned in recent times [from it's previous home on Google Code](https://code.google.com/p/fuzzdb/) so this is a revamp of it. Refer to the original [licenses](#License) for legal questions (or contact me). I'm working on a pretty large overhaul of its contents.

#### Introduction

Too much new software is vulnerable to the attack sequences of yesteryear. This suggests a testing approach: a comprehensive set of known attack pattern sequences can be leveraged for use in targeted fuzzing when testing for exploitable conditions in new applications.

This is especially useful for many filter bypass type exploits. Identical encoding sequences have been observed to bypass filters for more than one application. Examples can be observed in categories including xss, sqli, evil script upload, OS command execution, traversal issues, directory indexing bugs, source code revealing vulnerabilities, etc. In recent times, for example, new embedded webservers were discovered to be vulnerable to directory traversal issues triggered by encodings that exploited Microsoft IIS in 2000. This largely happens because the same high-level ideas are re-implemented or "approved upon" in the new language of the month, without a deep care for the fundamental risks involved.

This approach is also useful for targeted use of brute force for discovery using, for example, lists of known vulnerable scripts sorted by platform type, default locations of critical files of popular apps, high quality lists of common directory names.

The original sources primary sources used for attack pattern research:

- pesearching old web exploits for repeatable attack strings
- penetration tests
- scraping scanner patterns from my own http logs
- various books, articles, blog posts
- documentation for popular applications
- analysis of default application installs

Notable sources and other contributors:

- metasploit wmap http://www.metasploit.com/redmine/projects/framework/wiki/WMAP
- dirb http://www.open-labs.org/
- jbrofuzz http://www.owasp.org/index.php/Category:OWASP_JBroFuzz
- skipfish http://code.google.com/p/skipfish/
- rsnake's xss and rfi files http://ha.ckers.org/
- michael daw's web shell archive http://michaeldaw.org/
- joseph giron (joseph.giron13 (at) gmail.com)
- ron gutierrez - html tags and javascript events
- analysis of default app installs
- lists already submitted to OWASP Fuzzing Code DB by Wagner Elias, Eduardo Neves, Ulisses Castro, Adam Muntner http://www.owasp.org/index.php/Category:OWASP_Fuzzing_Code_Database#tab=News

Some files are derived primarily from other fuzzers, and are credited in the files with comments formatted like:

#### Table of Contents

  - [Assumption Checking](docs/assumptions.md)
  - [Brute Force Attacks](docs/brute-force.md)
  - [Denial of Service Attacks](docs/denial-of-service.md)
  - [Error Bounds Attacks](docs/error-bounds.md)
  - [Failed Crypto](docs/failed-crypto.md)
  - [Firewalls](docs/firewalls.md)
  - [Intrusion Detection](docs/intrusion-detection.md)
  - [Injection Attacks](docs/injection-attacks.md)
  - [Malformed / Missing Authentication](docs/malformed-auth.md)
  - [Overflow / Underflow Attacks](docs/overflow.md)
  - [Parsing Data](docs/parsing-data.md)
  - [Phishing Attacks](docs/phishing.md)
  - [Physical Compromise](docs/physical-compromise.md)
  - [Privilege escalation](docs/privilege-escalation.md)
  - [Race Conditions](docs/race-conditions.md)
  - [Relay Attacks](docs/relay-attacks.md)
  - [Replay Attacks](docs/replay-attacks.md)
  - [Session Hijacking](docs/session-hijacking.md)
  - [Scanners](docs/scanners.md)
  - [Sloppy Practices](docs/sloppy.md)
  - [Spoofing Attacks](docs/social-engineering.md)
  - [Social Engineering](docs/spoofing.md)
  - [Timing Attacks](docs/timing-attacks.md)

#### Download / Contribute

1. Check out via github: `git clone git@github.com:adamdecaf/fuzzdb.git`
1. Create a branch and submit a Pull Request

#### License

On the previous [project home on Google Code](https://code.google.com/p/fuzzdb/) the contents of this repository were licensed under the following:

- Code: http://opensource.org/licenses/BSD-3-Clause
- Content: https://creativecommons.org/licenses/by/3.0/

#### Contributors

- Adam Muntner <unix23@gmail.com>
- Adam Shannon <adam@ashannon.us>
