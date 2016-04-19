# vulnerabilities

> A collection of preventions against vulnerabilities in software.

### Introduction

All software has bugs. Some "bugs" are exploitable in ways that can cause great havoc with the data that they process or other systems they interact with. This is an attempt to make a concise listing of strategies and libraries which limit the range of vulnerabilities in software. Many techniques have been discovered throughout the years, and many counter measures are available and open source.

### Table of Contents

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
  - [Tracking](docs/tracking.md)

### Download / Contribute

1. Check out via github
1. Create a branch and submit a Pull Request

### License

This project was originally inspired from [fuzzdb](https://code.google.com/p/fuzzdb/) (now on [github](https://github.com/fuzzdb-project/fuzzdb))! I'm in the process of setting up a much better table of contributions and their specific licensing per-contributiion.

Most contributions are distilled down to the following licenses.

- Code: http://opensource.org/licenses/BSD-3-Clause
- Content: https://creativecommons.org/licenses/by/3.0/

### Contributors

- Adam Muntner <unix23@gmail.com>
- Adam Shannon <adam@ashannon.us>

Notable sources and other contributors: (From original fuzzdb)

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
