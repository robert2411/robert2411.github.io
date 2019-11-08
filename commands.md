[Home](./index) | [links](./links) | [Configurations](./configurations) | [Scripts](./scripts) | Commands

# Handy Commands

## Docker
 - `docker stats --all`
 - `docker run -it --pid=container:container:<contianer id> ubuntu`
 - `docker run -it --net=container:<container id> ubuntu`
 - `docker run -it --pid=host ubuntu`
 - `docker run -it --cap-drop=all ubuntu`
 - `--read-only --tempfs=/dir/subdir/`

## Git 
 - `git update-index --chmod=+x script.sh`
 - `git checkout -- file-to-reset`

## Jira
 - My open issues: `assignee = currentUser() AND resolution = Unresolved order by updated DESC`
 - Reported by me: `reporter = currentUser() order by created DESC`
 - Assigned to me: `assignee = currentUser() AND Sprint in openSprints() ORDER BY priority DESC, updated DESC`
 - watching: `watcher = currentUser() AND resolution = Unresolved ORDER BY priority DESC, updated DESC`

## Linux
 - Write to stdout of another proccess `echo "here" > /proc/<process id>/fd/[0 =stdin, 1, stdout, 2 stderror],` e.g. : `echo "here" > /proc/1/fd/1`
 
### CentOs
 - Install rpm from ulr: `yum install -y <URL>`
 - Find big files/folder `sudo du -h / | grep '[0-9\.]\+G'`

