# This is the human/machine readable list of Mozilla Media team triagers and dates each one is on duty

## To read the triage list and calendar
 Refer to regularly updated JSON file [triage.json](https://nils-ohlmeier.github.io/triage-list/triage.json) with list of names and bugzilla emails, and a calendar with duty end-dates.
- `"triagers"` root object node holds a map of `"Full Name" -> { data }`.  Right now the `data` object keeps only the bugzilla email in `bzmail` field.
- `"duty-end-dates"` root holds a map of `date -> "Full Name"`, where the `date` is the last day the triager is on duty, inclusive.  The last date is `2035-01-01` pointing at the `Fallback` triager.  Getting there means the list has to be manually updated and re-published.

## To add Media triagers in to your google calendar
Just use [this link to add it to gcal](https://calendar.google.com/calendar/r?cid=http://nils-ohlmeier.github.io/triage-list/media-triage.ics) and follow instructions.  The direct link to the ICS file is [here](https://nils-ohlmeier.github.io/triage-list/media-triage.ics).

## To update the triage list
```
git clone https://github.com/nils-ohlmeier/triage-list.git
cd triage-list
npm install
npm run update
npm run push
```

`npm run update` will automatically append the next full cycle of all triagers to the `triage.json` file.  `npm run push` will update the ICS file and `git push` the changes.  Then you are done.

If you already cloned before, then `update` and `push` commands are enough to publicly update the list.

Run `npm run help` for the full list of commands.
