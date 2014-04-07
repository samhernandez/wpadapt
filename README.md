WordPress Adapt
---

A simple executable to adapt an sql file dumped from WordPress from one domain to another. There are several robust tools out there that do this already. I just needed something quick, simple, and database-independent. This should work as a search/replace on any sql file with or without serialized data.

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

Tested on a 15mb file, it runs in less than a second.

Improvements and suggestions welcome!
