[Home](./index) | [Links](./links) | [Configurations](./configurations) | Scripts | [Commands](./commands)

# Handy scripts

## save the last git commits to a file to generate raw release notes + create a file with all the jira issues
```
#!/usr/bin/env bash
BUILD_VERSION=$1
echo ${BUILD_VERSION}

git log $(git describe --tags --abbrev=0)..HEAD --oneline | cut -d' ' -f 2- >> release-notes-${BUILD_VERSION}.txt

rm -r jira-raw.txt
cat release-notes-${BUILD_VERSION}.txt| grep -oP '[A-Z]+-[0-9]+' >> jira-raw.txt
sort jira-raw.txt | uniq >> release-notes-${BUILD_VERSION}-jira.txt
```
### Wait until docker-compose up is done
```
#!/bin/bash

cd evs-via

while [ $(docker-compose ps | grep starting | wc -l) -ne 0 ]
do
echo "System is starting"
echo $(docker-compose ps | grep starting | wc -l)
sleep 1m
done
echo "System started"
```
