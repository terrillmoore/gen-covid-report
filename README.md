# gen-covid-report

Script for generating COVID-19 reports from JHU data. Updated 30-day daily reports available at [terrillmoore.github.io/gen-covid-report/](https://terrillmoore.github.io/gen-covid-report/).

## Use

I put this repo in a directory next to the Johns Hopkins [COVID-19](https://github.com/CSSEGISandData/COVID-19) database.
I use the following command line (in git bash) to generate the reports.

```bash
MCCIBRIGHT_LIB=c:/tools/lib/bright /c/tools/bin/bright gen-covid-report.bri ../COVID-19/ 30 > docs/index.md
```

The command line arguments are positional. The first argument is the path to the clone of the COVID-19 repository. The second argument is the number of days of history to print. Output always comes to standard out, and in this case is redirected to the GitHub pages `index.md` file.

It's often convenient to do a test run with 5 or 10 days when a new database image is downloaded, just to check whether anything has changed that breaks things.

## Changes

### 2020-03-23

JHU introduced a new schema for data and stopped updating some of the older files. Changes included:

- obsoleting `time_series_19-covid-Confirmed.csv`, `time_series_19-covid-Deaths.csv`, and `time_series_19-covid-Recovered.csv`
- new tables without US detail data `time_series_covid19_confirmed_global.csv` and `time_series_covid19_deaths_global.csv`.

Notice that there's no "recovered" data in the new files.

The script changed to read the new files, and to zero out the recovery data (for now).

At some point, this script will switch to reading the new daily files. However, the internal schema for the daily files also changed on 03-23; the columns changed radically, county-by-county data was added in the US, and a FIPS code was added for each US county. Prior to 03-23 the data may have been grouped by county, but the grouping was not as rigorous (or complete -- all counties seem to be listed, whether they have reported cases or not). We will wait for a day or two before converting.

Git diff on `docs/index.md` shows that some of the data has been updated, and the numbers are slightly (but not materially) different.
