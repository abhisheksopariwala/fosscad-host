defcad-host
===========

Generates a website that will update itself with the lastest from defcad-repo.

#### Instructions

Currently the best way to do this is:

```bash
:~$ cd ~/
:~$ git clone https://github.com/maduce/defcad-host.git
:~$ cd defcad-host
:~$ git clone https://github.com/maduce/defcad-repo.git
```

Note: If you already have a defcad-repo, you can copy or move it to ~/defcad-host/ instead of recloning it.

Next you can edit ```~/defcad-host/config.cfg``` if you desire.  The default configs assume the defcad-host folder is in ```~/``` so you can avoid changing the configs and move on to the next step if you followed the above instructions.  To create the database and a zipped version of the repo (~/defcad-host/web/www/zippedpack/):
```bash
:~$ sh hostpack.sh --generate 
```
To update the zippedpack and database:
```bash
:~$ sh hostpack.sh --update
```
See ~/defcad-repo/hostpack.sh for more options.  To delete the zippedpack and the database (i.e., starting from scratch, but not deleting the ~/defcad-host/defcad-repo/ folder), run: 
```bash
:~$ sh hostpack.sh --delete
```
If you use --delete you will need to generate the zippedpack again before you update.

Note: This is VERY MUCH a work in progress and has little use at this time.
