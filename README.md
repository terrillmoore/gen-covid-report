# gen-covid-report

Script for generating COVID-19 reports from JHU data. Updated 30-day daily reports available at [`terrillmoore.github.io/gen-covid-report/`](https://terrillmoore.github.io/gen-covid-report/).

<!--
  This TOC uses the VS Code markdown TOC extension AlanWalk.markdown-toc.
  We strongly recommend updating using VS Code, the markdown-toc extension and the
  bierner.markdown-preview-github-styles extension. Note that if you are using
  VS Code 1.29 and Markdown TOC 1.5.6, https://github.com/AlanWalk/markdown-toc/issues/65
  applies -- you must change your line-ending to some non-auto value in Settings>
  Text Editor>Files.  `\n` works for me.
-->
<!-- markdownlint-disable MD033 MD004 -->
<!-- markdownlint-capture -->
<!-- markdownlint-disable -->
<!-- TOC depthFrom:2 updateOnSave:true -->

- [Using the Script](#using-the-script)
- [Changes](#changes)
    - [2020-03-24](#2020-03-24)
    - [2020-03-23](#2020-03-23)

<!-- /TOC -->
<!-- markdownlint-restore -->
<!-- Due to a bug in Markdown TOC, the table is formatted incorrectly if tab indentation is set other than 4. Due to another bug, this comment must be *after* the TOC entry. -->

## Using the Script

Put this repo in a directory next to the Johns Hopkins [COVID-19](https://github.com/CSSEGISandData/COVID-19) database.
Use the following command line (in git bash) to generate the reports.

```bash
MCCIBRIGHT_LIB=c:/tools/lib/bright /c/tools/bin/bright gen-covid-report.bri ../COVID-19/ 30 > docs/index.md
```

The command line arguments are positional. The first argument is the path to the clone of the COVID-19 repository. The second argument is the number of days of history to print. Output always comes to standard out, and in this case is redirected to the GitHub pages `index.md` file.

It's often convenient to do a test run with 5 or 10 days when a new database image is downloaded, just to check whether anything has changed that breaks things.

## Changes

### 2020-03-24

No changes in the database format or the script today.

### 2020-03-23

JHU introduced a new schema for data and stopped updating some of the older files. Changes included:

- obsoleting `time_series_19-covid-Confirmed.csv`, `time_series_19-covid-Deaths.csv`, and `time_series_19-covid-Recovered.csv`
- new tables without US detail data `time_series_covid19_confirmed_global.csv` and `time_series_covid19_deaths_global.csv`.

Notice that there's no "recovered" data in the new files.

The script changed to read the new files, and to zero out the recovery data (for now).

At some point, this script will switch to reading the new daily files. However, the internal schema for the daily files also changed on 03-23; the columns changed radically, county-by-county data was added in the US, and a FIPS code was added for each US county. Prior to 03-23 the data may have been grouped by county, but the grouping was not as rigorous (or complete -- all counties seem to be listed, whether they have reported cases or not). We will wait for a day or two before converting.

Git diff on `docs/index.md` shows that some of the data has been updated, and the numbers are slightly (but not materially) different.
