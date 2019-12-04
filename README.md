

see https://github.com/Neo23x0/auditd

and https://github.com/bfuzzy/auditd-attack/blob/master/auditd-attack.rules

see fields https://github.com/linux-audit/audit-documentation/blob/master/specs/fields/field-dictionary.csv

TODO
----

* try to filter out localhost connections from processes that have business together (eg postfix uses dovecot for auth, etc.)
* filter out UDP 53 (DNS queries)
* create rules that match shell executions (though there's already root_execve, so eventually everything is covered)
* filter out things that root does but is expected (eg started from cron)
* wrap augenrules --load and instead of hardcoding postfix UID get it from /etc/passwd .. :|

