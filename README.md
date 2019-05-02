# Rolling Files
a bash script for file rotation

## How to use?

```

> rolling-files \
   --source-path /mnt/my-data/ \
   --dest-path ~/archives/ \
   --file-pattern "backup_[[:digit:]]{8}\.zip" \
   --keep-N 2

IS VERBOSE? false
AUTO YES? false
DRY RUN? false
SOURCE PATH: /mnt/my-data/
DEST PATH: /home/siutin/archives/
PATTERN: backup_[[:digit:]]{8}\.zip
KEEP N: 2
***************** start - Thu May 2 00:47:18 HKT 2019 ****************
NUM OF FILES TO MOVE: 5
FILES TO MOVE:
         backup_daily_20190425.zip
         backup_daily_20190426.zip
         backup_daily_20190427.zip
         backup_daily_20190428.zip
         backup_daily_20190429.zip
FILES TO KEEP:
         backup_daily_20190430.zip
         backup_daily_20190501.zip
Are you sure you want to continue? [Y/n] Y
Y.
sending incremental file list
backup_20190425.zip
              0 100%    0.00kB/s    0:00:00 (xfr#1, to-chk=4/5)
backup_20190426.zip
              0 100%    0.00kB/s    0:00:00 (xfr#2, to-chk=3/5)
backup_20190427.zip
              0 100%    0.00kB/s    0:00:00 (xfr#3, to-chk=2/5)
backup_20190428.zip
              0 100%    0.00kB/s    0:00:00 (xfr#4, to-chk=1/5)
backup_20190429.zip
              0 100%    0.00kB/s    0:00:00 (xfr#5, to-chk=0/5)

sent 347 bytes  received 151 bytes  996.00 bytes/sec
total size is 0  speedup is 0.00
***************** end - Thu May 2 00:47:20 HKT 2019 ****************  
```

## Manual

```

Usage: rolling-files [ARGUMENTS]

Required Arguments:

 --source-path <argument>
 
  Specify the path to the source directory.
  
 --dest-path <argument>
 
  Specify the path to the destination directory.

Optional Arguments:

 --keep-N <argument>
 
  Keep the N most recent files. Default 3.
 
 --file-pattern <PATTERN>
  
  Filter files by using grep extended regular expressions.
 
 --auto-yes
 
  Automatic yes to prompts; assume "yes" as answer to all prompts and run non-interactively.
 
 --dry-run
 
  Perform a trial run with no changes made.
 
 --verbose
 
  Increase the verbosity.
 
 --help or -h or -?
  Display the manaual page for the command.
```

---

## Contributors
 [Martin Chan](https://twitter.com/osiutino) - creator 

## License

[MIT](https://opensource.org/licenses/MIT)
