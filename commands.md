[Home](./index) | [links](./links) | [Configurations](./configurations) | Commands
# Handy Commands

## Docker
 - `docker stats --all`

## Git 
 - `git update-index --chmod=+x script.sh`
 - `git checkout -- file-to-reset`

## Jira
 - My open issues: `assignee = currentUser() AND resolution = Unresolved order by updated DESC`
 - Reported by me: `reporter = currentUser() order by created DESC`
 - Assigned to me: `assignee = currentUser() AND Sprint in openSprints() ORDER BY priority DESC, updated DESC`
 - watching: `watcher = currentUser() AND resolution = Unresolved ORDER BY priority DESC, updated DESC`
