NEVER EVER TRUST user input
- link to imgmi.net

- not checking certain conditions
- mime types / based on file extension
- check "header bytes" of files
 - images, video, etc

- assuming a certain encoding

- not normalizing data
  - file paths ("../../../")
  - counters
  - mutable state
  - proxy / redirect urls
    - https://www.gnu.gl/blog/Posts/multiple-vulnerabilities-in-pocket/

https://en.wikipedia.org/wiki/Directory_traversal_attack (from scanners)

https://github.com/benjamingr/favicon-bug
