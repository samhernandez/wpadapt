WordPress Adapt
---

A tool to adapt an sql file dumped from WordPress from one domain to another.

Put the `wpadapt` executable file somewhere in your system path.

Running `wpadapt` with no arguments shows this usage information:

```
usage: wpadapt [-i] -search=value -replace=value source_file target_file

options:

  -search, -s     Required search term to replace.
                  e.g. -s=remote.domain.com

  -replace, -r    Required replacement value for the search term.
                  e.g. -r=local.domain.dev

  -i              Optional. Triggers a case-insensitive search/replace.

examples:

  wpadapt -search=old.domain.com -replace=new.domain.dev remote_db.sql local_db.sql
  wpadapt -s=old.domain.com -f=new.domain.dev remote_db.sql local_db.sql
  wpadapt -s=OLD.DOMAIN.COM -f=new.domain.dev -i remote_db.sql local_db.sql
```

Improvements and suggestions welcome!
