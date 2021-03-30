# Tracking pages changes on the Department of Defense Forms Management Program pages

A git scraper designed to grab the latest changes from the source code of all DoD Forms Management index pages (links labeled in the section titled "DD Forms"):

![boop](https://raw.githubusercontent.com/RooneyMcNibNug/DoD-Forms-Page-Diffs/main/Screenshot_2021-03-14%20DoD%20Forms%20Management.png)

This includes the nice tables they have set with Number, Title, Edition Date, and OPR columns. Currently, `wget` is used to grab a full HTML copy of the source code from each DD Forms page and putput into a labelled HTML file in the repo. Directly afterwards, `w3m` is used with the `-dump` param to grab a "cleaner" body of all DD Forms pages and output to a .txt file for each.

The cron in the scraper config is currently set to check daily for changes.

I thought this might be useful for FOIA folx as well as more generally tracking the changes on these directives for more automated transparency. Diffs are your friend.
