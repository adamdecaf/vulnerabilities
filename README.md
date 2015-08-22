**fuzzdb**: Web Fuzzing Discovery and Attack Pattern Database

#### Notice

This project seems to have been fairly abandoned in recent times [from it's previous home on Google Code](https://code.google.com/p/fuzzdb/) so this is a revamp of it. Refer to the original [licenses](#License) for legal questions (or contact me).

#### Introduction

Too much new software is vulnerable to the attack sequences of yesteryear. This suggests a testing approach: a comprehensive set of known attack pattern sequences can be leveraged for use in targeted fuzzing when testing for exploitable conditions in new applications.

This is especially useful for many filter bypass type exploits. Identical encoding sequences have been observed to bypass filters for more than one application. Examples can be observed in categories including xss, sqli, evil script upload, OS command execution, traversal issues, directory indexing bugs, source code revealing vulnerabilities, etc. In recent times, for example, new embedded webservers were discovered to be vulnerable to directory traversal issues triggered by encodings that exploited Microsoft IIS in 2000.

This approach is also useful for targeted use of brute force for discovery using, for example, lists of known vulnerable scripts sorted by platform type, default locations of critical files of popular apps, high quality lists of common directory names.

Primary sources used for attack pattern research:

- researching old web exploits for repeatable attack strings
- penetration tests i've performed in the past
- scraping scanner patterns from my own http logs
- various books, articles, blog posts
- documentation for popular applications
- analysis of default application installs

notable sources and other contributors:

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

##### This file is primarily derived from source xyz

Others have additional instructions for payload use in a similar comment format at the top of the file

#### Download

Check out via github:

```
git clone git@github.com:adamdecaf/fuzzdb.git
```

#### License

On the previous [project home on Google Code](https://code.google.com/p/fuzzdb/) the contents of this repository were licensed under the following:

- Code: http://opensource.org/licenses/BSD-3-Clause
- Content: https://creativecommons.org/licenses/by/3.0/

#### Contributors

- Adam Muntner <unix23@gmail.com>
