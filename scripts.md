```
#!/usr/bin/env bash
BUILD_VERSION=$1
echo ${BUILD_VERSION}

git log $(git describe --tags --abbrev=0)..HEAD --oneline | cut -d' ' -f 2- >> release-notes-${BUILD_VERSION}.txt

rm -r jira-raw.txt
cat release-notes-${BUILD_VERSION}.txt| grep -oP '[A-Z]+-[0-9]+' >> jira-raw.txt
sort jira-raw.txt | uniq >> release-notes-${BUILD_VERSION}-jira.txt
```
