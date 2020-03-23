# COVID-19 Report from `gen-covid-report`

This report was generated from the Johns Hopkins COVID-19 data base, available on [GitHub](https://github.com/CSSEGISandData/COVID-19).

It consists of reports about a number of countries, followed by a slightly different report on world data.

The country data starts with data for South Korea, which is taken as reference for relating cases to death rate during a well-surveilled outbreak.

Other countries are then presented, with comparisons to South Korea where applicable.

The report columns and their meanings:

- **Date** is the date of the report.
- **Dn** is the index relative to day when cases reached 100 or more. Days before 100 cases were reached are taken as negative. Following a suggestion I found at ft.com, a case load of 100 cases is taken to indicate the onset of community transition.
- **Confirmed** is the number of confirmed cases from the JHU COVID-19 series.
- **Deaths** is the number of reported deaths from the JHU COVID-19 series.
- **Pop/Confirmed** is the number of people per case in that country. Lower numbers indicate higher case load. I use this because it's easier to relate to community populations in a subset of the population. It might also be nice to report log(cases/population), which I imagine is the way it's ordinarily reported.
- **Doubling** is the number of days between doubling. It's not smoothed at all. Delays in reporting data will occasionally perturb it.
- **Deaths (%)** is simply reported deaths over reported cases, times 100%.
- **KR Deaths (%)** is the reference death rate in Korea _on the same relative day of outbreak_.
- **Inferred Cases** is the calculated number of cases, in case the reported death rate is higher than the Korean rate on the same day of the outbreak. This number is based on dividing the reported number of deaths by the reference Korean death rate. It's only reported if the Korean death rate is lower than the country's death rate.
- **Inferred Pop/Confirmed** is simply the number of people per inferred case.

The program for generating this report can be found on GitHub at [github.com/terrillmoore/gen-covid-report](https://github.com/terrillmoore/gen-covid-report). Running it requires a copy of the author's dialect of Lua, called "bright". Binaries are in the repository; [file an issue](https://github.com/terrillmoore/gen-covid-report/issues) if you'd like to encourage publication of the tools used in this script, or feel free to convert to Python, Lua, or the scripting language of your choice.

## Korea, South Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | 1 | 204 | 2 | 250,000 | 1.0 | 0.98 | 0.98 | - | - |
| 2020-02-22 | 2 | 433 | 2 | 117,782 | 0.9 | 0.46 | 0.46 | - | - |
| 2020-02-23 | 3 | 602 | 6 | 84,717 | 2.1 | 1.00 | 1.00 | - | - |
| 2020-02-24 | 4 | 833 | 8 | 61,224 | 2.1 | 0.96 | 0.96 | - | - |
| 2020-02-25 | 5 | 977 | 10 | 52,200 | 4.3 | 1.02 | 1.02 | - | - |
| 2020-02-26 | 6 | 1,261 | 12 | 40,444 | 2.7 | 0.95 | 0.95 | - | - |
| 2020-02-27 | 7 | 1,766 | 13 | 28,878 | 2.1 | 0.74 | 0.74 | - | - |
| 2020-02-28 | 8 | 2,337 | 13 | 21,822 | 2.5 | 0.56 | 0.56 | - | - |
| 2020-02-29 | 9 | 3,150 | 16 | 16,190 | 2.3 | 0.51 | 0.51 | - | - |
| 2020-03-01 | 10 | 3,736 | 17 | 13,650 | 4.1 | 0.46 | 0.46 | - | - |
| 2020-03-02 | 11 | 4,335 | 28 | 11,764 | 4.7 | 0.65 | 0.65 | - | - |
| 2020-03-03 | 12 | 5,186 | 28 | 9,834 | 3.9 | 0.54 | 0.54 | - | - |
| 2020-03-04 | 13 | 5,621 | 35 | 9,073 | 8.6 | 0.62 | 0.62 | - | - |
| 2020-03-05 | 14 | 6,088 | 35 | 8,377 | 8.7 | 0.57 | 0.57 | - | - |
| 2020-03-06 | 15 | 6,593 | 42 | 7,735 | 8.7 | 0.64 | 0.64 | - | - |
| 2020-03-07 | 16 | 7,041 | 44 | 7,243 | 10.5 | 0.62 | 0.62 | - | - |
| 2020-03-08 | 17 | 7,314 | 50 | 6,972 | 18.2 | 0.68 | 0.68 | - | - |
| 2020-03-09 | 18 | 7,478 | 53 | 6,820 | 31.3 | 0.71 | 0.71 | - | - |
| 2020-03-10 | 19 | 7,513 | 54 | 6,788 | 148.4 | 0.72 | 0.72 | - | - |
| 2020-03-11 | 20 | 7,755 | 60 | 6,576 | 21.9 | 0.77 | 0.77 | - | - |
| 2020-03-12 | 21 | 7,869 | 66 | 6,481 | 47.5 | 0.84 | 0.84 | - | - |
| 2020-03-13 | 22 | 7,979 | 66 | 6,391 | 49.9 | 0.83 | 0.83 | - | - |
| 2020-03-14 | 23 | 8,086 | 72 | 6,307 | 52.0 | 0.89 | 0.89 | - | - |
| 2020-03-15 | 24 | 8,162 | 75 | 6,248 | 74.1 | 0.92 | 0.92 | - | - |
| 2020-03-16 | 25 | 8,236 | 75 | 6,192 | 76.8 | 0.91 | 0.91 | - | - |
| 2020-03-17 | 26 | 8,320 | 81 | 6,129 | 68.3 | 0.97 | 0.97 | - | - |
| 2020-03-18 | 27 | 8,413 | 84 | 6,062 | 62.4 | 1.00 | 1.00 | - | - |
| 2020-03-19 | 28 | 8,565 | 91 | 5,954 | 38.7 | 1.06 | 1.06 | - | - |
| 2020-03-20 | 29 | 8,652 | 94 | 5,894 | 68.6 | 1.09 | 1.09 | - | - |
| 2020-03-21 | 30 | 8,799 | 102 | 5,796 | 41.1 | 1.16 | 1.16 | - | - |

## US Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -11 | 15 | 0 | 22.0e6 | 4.8 | 0.00 | 0.00 | - | - |
| 2020-02-22 | -10 | 15 | 0 | 22.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-23 | -9 | 15 | 0 | 22.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-24 | -8 | 51 | 0 | 6.5e6 | 0.6 | 0.00 | 0.00 | - | - |
| 2020-02-25 | -7 | 51 | 0 | 6.5e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-26 | -6 | 57 | 0 | 5.8e6 | 6.2 | 0.00 | 0.00 | - | - |
| 2020-02-27 | -5 | 58 | 0 | 5.7e6 | 39.9 | 0.00 | 0.00 | - | - |
| 2020-02-28 | -4 | 60 | 0 | 5.5e6 | 20.4 | 0.00 | 0.00 | - | - |
| 2020-02-29 | -3 | 68 | 1 | 4.9e6 | 5.5 | 1.47 | 0.00 | - | - |
| 2020-03-01 | -2 | 74 | 1 | 4.5e6 | 8.2 | 1.35 | 0.00 | - | - |
| 2020-03-02 | -1 | 98 | 6 | 3.4e6 | 2.5 | 6.12 | 0.00 | - | - |
| 2020-03-03 | 0 | 118 | 7 | 2.8e6 | 3.7 | 5.93 | 0.96 | 728 | 453,296 |
| 2020-03-04 | 1 | 149 | 11 | 2.2e6 | 3.0 | 7.38 | 0.98 | 1,122 | 294,117 |
| 2020-03-05 | 2 | 217 | 12 | 1.5e6 | 1.8 | 5.53 | 0.46 | 2,598 | 127,020 |
| 2020-03-06 | 3 | 262 | 14 | 1.3e6 | 3.7 | 5.34 | 1.00 | 1,404 | 234,931 |
| 2020-03-07 | 4 | 402 | 17 | 820,895 | 1.6 | 4.23 | 0.96 | 1,770 | 186,427 |
| 2020-03-08 | 5 | 518 | 21 | 637,065 | 2.7 | 4.05 | 1.02 | 2,051 | 160,842 |
| 2020-03-09 | 6 | 583 | 22 | 566,037 | 5.9 | 3.77 | 0.95 | 2,311 | 142,743 |
| 2020-03-10 | 7 | 795 | 28 | 415,094 | 2.2 | 3.52 | 0.74 | 3,803 | 86,757 |
| 2020-03-11 | 8 | 1,109 | 36 | 297,565 | 2.1 | 3.25 | 0.56 | 6,471 | 50,991 |
| 2020-03-12 | 9 | 1,478 | 40 | 223,274 | 2.4 | 2.71 | 0.51 | 7,875 | 41,904 |
| 2020-03-13 | 10 | 1,979 | 47 | 166,750 | 2.4 | 2.37 | 0.46 | 10,328 | 31,949 |
| 2020-03-14 | 11 | 2,512 | 54 | 131,369 | 2.9 | 2.15 | 0.65 | 8,360 | 39,471 |
| 2020-03-15 | 12 | 3,252 | 63 | 101,476 | 2.7 | 1.94 | 0.54 | 11,668 | 28,281 |
| 2020-03-16 | 13 | 4,346 | 85 | 75,931 | 2.4 | 1.96 | 0.62 | 13,651 | 24,174 |
| 2020-03-17 | 14 | 6,113 | 108 | 53,983 | 2.0 | 1.77 | 0.57 | 18,785 | 17,566 |
| 2020-03-18 | 15 | 7,466 | 118 | 44,200 | 3.5 | 1.58 | 0.64 | 18,523 | 17,815 |
| 2020-03-19 | 16 | 13,240 | 200 | 24,924 | 1.2 | 1.51 | 0.62 | 32,004 | 10,311 |
| 2020-03-20 | 17 | 18,544 | 242 | 17,795 | 2.1 | 1.31 | 0.68 | 35,399 | 9,322 |
| 2020-03-21 | 18 | 24,815 | 305 | 13,298 | 2.4 | 1.23 | 0.71 | 43,033 | 7,668 |

## Italy Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -2 | 20 | 1 | 3.1e6 | 0.4 | 5.00 | 0.00 | - | - |
| 2020-02-22 | -1 | 62 | 2 | 1.0e6 | 0.6 | 3.23 | 0.00 | - | - |
| 2020-02-23 | 0 | 155 | 3 | 400,000 | 0.8 | 1.94 | 0.96 | 312 | 198,717 |
| 2020-02-24 | 1 | 229 | 7 | 270,742 | 1.8 | 3.06 | 0.98 | 714 | 86,834 |
| 2020-02-25 | 2 | 322 | 10 | 192,546 | 2.0 | 3.11 | 0.46 | 2,165 | 28,637 |
| 2020-02-26 | 3 | 453 | 12 | 136,865 | 2.0 | 2.65 | 1.00 | 1,204 | 51,495 |
| 2020-02-27 | 4 | 655 | 17 | 94,656 | 1.9 | 2.60 | 0.96 | 1,770 | 35,025 |
| 2020-02-28 | 5 | 888 | 21 | 69,819 | 2.3 | 2.36 | 1.02 | 2,051 | 30,218 |
| 2020-02-29 | 6 | 1,128 | 29 | 54,964 | 2.9 | 2.57 | 0.95 | 3,047 | 20,345 |
| 2020-03-01 | 7 | 1,694 | 34 | 36,599 | 1.7 | 2.01 | 0.74 | 4,618 | 13,423 |
| 2020-03-02 | 8 | 2,036 | 52 | 30,451 | 3.8 | 2.55 | 0.56 | 9,348 | 6,632 |
| 2020-03-03 | 9 | 2,502 | 79 | 24,780 | 3.4 | 3.16 | 0.51 | 15,553 | 3,986 |
| 2020-03-04 | 10 | 3,089 | 107 | 20,071 | 3.3 | 3.46 | 0.46 | 23,514 | 2,636 |
| 2020-03-05 | 11 | 3,858 | 148 | 16,070 | 3.1 | 3.84 | 0.65 | 22,913 | 2,705 |
| 2020-03-06 | 12 | 4,636 | 197 | 13,373 | 3.8 | 4.25 | 0.54 | 36,487 | 1,699 |
| 2020-03-07 | 13 | 5,883 | 233 | 10,538 | 2.9 | 3.96 | 0.62 | 37,419 | 1,656 |
| 2020-03-08 | 14 | 7,375 | 366 | 8,406 | 3.1 | 4.96 | 0.57 | 63,663 | 973 |
| 2020-03-09 | 15 | 9,172 | 463 | 6,759 | 3.2 | 5.05 | 0.64 | 72,679 | 853 |
| 2020-03-10 | 16 | 10,149 | 631 | 6,108 | 6.8 | 6.22 | 0.62 | 100,974 | 614 |
| 2020-03-11 | 17 | 12,462 | 827 | 4,975 | 3.4 | 6.64 | 0.68 | 120,973 | 512 |
| 2020-03-12 | 18 | 12,462 | 827 | 4,975 | -  | 6.64 | 0.71 | 116,685 | 531 |
| 2020-03-13 | 19 | 17,660 | 1,266 | 3,510 | 2.0 | 7.17 | 0.72 | 176,138 | 351 |
| 2020-03-14 | 20 | 21,157 | 1,441 | 2,930 | 3.8 | 6.81 | 0.77 | 186,249 | 332 |
| 2020-03-15 | 21 | 24,747 | 1,809 | 2,505 | 4.4 | 7.31 | 0.84 | 215,682 | 287 |
| 2020-03-16 | 22 | 27,980 | 2,158 | 2,215 | 5.6 | 7.71 | 0.83 | 260,889 | 237 |
| 2020-03-17 | 23 | 31,506 | 2,503 | 1,967 | 5.8 | 7.94 | 0.89 | 281,100 | 220 |
| 2020-03-18 | 24 | 35,713 | 2,978 | 1,736 | 5.5 | 8.34 | 0.92 | 324,085 | 191 |
| 2020-03-19 | 25 | 41,035 | 3,405 | 1,510 | 5.0 | 8.30 | 0.91 | 373,914 | 165 |
| 2020-03-20 | 26 | 47,021 | 4,032 | 1,318 | 5.1 | 8.57 | 0.97 | 414,151 | 149 |
| 2020-03-21 | 27 | 53,578 | 4,825 | 1,157 | 5.3 | 9.01 | 1.00 | 483,246 | 128 |

## Norway Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -14 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-22 | -13 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-23 | -12 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-24 | -11 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-25 | -10 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-26 | -9 | 1 | 0 | 5.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-27 | -8 | 1 | 0 | 5.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-28 | -7 | 6 | 0 | 866,666 | 0.4 | 0.00 | 0.00 | - | - |
| 2020-02-29 | -6 | 15 | 0 | 346,666 | 0.8 | 0.00 | 0.00 | - | - |
| 2020-03-01 | -5 | 19 | 0 | 273,684 | 2.9 | 0.00 | 0.00 | - | - |
| 2020-03-02 | -4 | 25 | 0 | 208,000 | 2.5 | 0.00 | 0.00 | - | - |
| 2020-03-03 | -3 | 32 | 0 | 162,500 | 2.8 | 0.00 | 0.00 | - | - |
| 2020-03-04 | -2 | 56 | 0 | 92,857 | 1.2 | 0.00 | 0.00 | - | - |
| 2020-03-05 | -1 | 87 | 0 | 59,770 | 1.6 | 0.00 | 0.00 | - | - |
| 2020-03-06 | 0 | 108 | 0 | 48,148 | 3.2 | 0.00 | 0.96 | - | - |
| 2020-03-07 | 1 | 147 | 0 | 35,374 | 2.2 | 0.00 | 0.98 | - | - |
| 2020-03-08 | 2 | 176 | 0 | 29,545 | 3.8 | 0.00 | 0.46 | - | - |
| 2020-03-09 | 3 | 205 | 0 | 25,365 | 4.5 | 0.00 | 1.00 | - | - |
| 2020-03-10 | 4 | 400 | 0 | 13,000 | 1.0 | 0.00 | 0.96 | - | - |
| 2020-03-11 | 5 | 598 | 0 | 8,695 | 1.7 | 0.00 | 1.02 | - | - |
| 2020-03-12 | 6 | 702 | 0 | 7,407 | 4.3 | 0.00 | 0.95 | - | - |
| 2020-03-13 | 7 | 996 | 0 | 5,220 | 2.0 | 0.00 | 0.74 | - | - |
| 2020-03-14 | 8 | 1,090 | 3 | 4,770 | 7.7 | 0.28 | 0.56 | - | - |
| 2020-03-15 | 9 | 1,221 | 3 | 4,258 | 6.1 | 0.25 | 0.51 | - | - |
| 2020-03-16 | 10 | 1,333 | 3 | 3,900 | 7.9 | 0.23 | 0.46 | - | - |
| 2020-03-17 | 11 | 1,463 | 3 | 3,554 | 7.4 | 0.21 | 0.65 | - | - |
| 2020-03-18 | 12 | 1,550 | 6 | 3,354 | 12.0 | 0.39 | 0.54 | - | - |
| 2020-03-19 | 13 | 1,746 | 7 | 2,978 | 5.8 | 0.40 | 0.62 | - | - |
| 2020-03-20 | 14 | 1,914 | 7 | 2,716 | 7.5 | 0.37 | 0.57 | - | - |
| 2020-03-21 | 15 | 2,118 | 7 | 2,455 | 6.8 | 0.33 | 0.64 | - | - |

## Spain Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -10 | 2 | 0 | 23.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-22 | -9 | 2 | 0 | 23.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-23 | -8 | 2 | 0 | 23.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-24 | -7 | 2 | 0 | 23.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-25 | -6 | 6 | 0 | 7.7e6 | 0.6 | 0.00 | 0.00 | - | - |
| 2020-02-26 | -5 | 13 | 0 | 3.6e6 | 0.9 | 0.00 | 0.00 | - | - |
| 2020-02-27 | -4 | 15 | 0 | 3.1e6 | 4.8 | 0.00 | 0.00 | - | - |
| 2020-02-28 | -3 | 32 | 0 | 1.5e6 | 0.9 | 0.00 | 0.00 | - | - |
| 2020-02-29 | -2 | 45 | 0 | 1.0e6 | 2.0 | 0.00 | 0.00 | - | - |
| 2020-03-01 | -1 | 84 | 0 | 552,619 | 1.1 | 0.00 | 0.00 | - | - |
| 2020-03-02 | 0 | 120 | 0 | 386,833 | 1.9 | 0.00 | 0.96 | - | - |
| 2020-03-03 | 1 | 165 | 1 | 281,333 | 2.2 | 0.61 | 0.98 | - | - |
| 2020-03-04 | 2 | 222 | 2 | 209,099 | 2.3 | 0.90 | 0.46 | 433 | 107,205 |
| 2020-03-05 | 3 | 259 | 3 | 179,227 | 4.5 | 1.16 | 1.00 | 301 | 154,219 |
| 2020-03-06 | 4 | 400 | 5 | 116,050 | 1.6 | 1.25 | 0.96 | 520 | 89,162 |
| 2020-03-07 | 5 | 500 | 10 | 92,840 | 3.1 | 2.00 | 1.02 | 976 | 47,512 |
| 2020-03-08 | 6 | 673 | 17 | 68,974 | 2.3 | 2.53 | 0.95 | 1,786 | 25,984 |
| 2020-03-09 | 7 | 1,073 | 28 | 43,261 | 1.5 | 2.61 | 0.74 | 3,803 | 12,203 |
| 2020-03-10 | 8 | 1,695 | 35 | 27,386 | 1.5 | 2.06 | 0.56 | 6,291 | 7,377 |
| 2020-03-11 | 9 | 2,277 | 54 | 20,386 | 2.3 | 2.37 | 0.51 | 10,631 | 4,366 |
| 2020-03-12 | 10 | 2,277 | 55 | 20,386 | -  | 2.42 | 0.46 | 12,087 | 3,840 |
| 2020-03-13 | 11 | 5,232 | 133 | 8,872 | 0.8 | 2.54 | 0.65 | 20,591 | 2,254 |
| 2020-03-14 | 12 | 6,391 | 195 | 7,263 | 3.5 | 3.05 | 0.54 | 36,116 | 1,285 |
| 2020-03-15 | 13 | 7,798 | 289 | 5,952 | 3.5 | 3.71 | 0.62 | 46,413 | 1,000 |
| 2020-03-16 | 14 | 9,942 | 342 | 4,669 | 2.9 | 3.44 | 0.57 | 59,488 | 780 |
| 2020-03-17 | 15 | 11,748 | 533 | 3,951 | 4.2 | 4.54 | 0.64 | 83,668 | 554 |
| 2020-03-18 | 16 | 13,910 | 623 | 3,337 | 4.1 | 4.48 | 0.62 | 99,694 | 465 |
| 2020-03-19 | 17 | 17,963 | 830 | 2,584 | 2.7 | 4.62 | 0.68 | 121,412 | 382 |
| 2020-03-20 | 18 | 20,410 | 1,043 | 2,274 | 5.4 | 5.11 | 0.71 | 147,161 | 315 |
| 2020-03-21 | 19 | 25,374 | 1,375 | 1,829 | 3.2 | 5.42 | 0.72 | 191,303 | 242 |

## France Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -8 | 12 | 1 | 5.6e6 | -  | 8.33 | 0.00 | - | - |
| 2020-02-22 | -7 | 12 | 1 | 5.6e6 | -  | 8.33 | 0.00 | - | - |
| 2020-02-23 | -6 | 12 | 1 | 5.6e6 | -  | 8.33 | 0.00 | - | - |
| 2020-02-24 | -5 | 12 | 1 | 5.6e6 | -  | 8.33 | 0.00 | - | - |
| 2020-02-25 | -4 | 14 | 1 | 4.8e6 | 4.5 | 7.14 | 0.00 | - | - |
| 2020-02-26 | -3 | 18 | 2 | 3.7e6 | 2.8 | 11.11 | 0.00 | - | - |
| 2020-02-27 | -2 | 38 | 2 | 1.8e6 | 0.9 | 5.26 | 0.00 | - | - |
| 2020-02-28 | -1 | 57 | 2 | 1.2e6 | 1.7 | 3.51 | 0.00 | - | - |
| 2020-02-29 | 0 | 100 | 2 | 669,000 | 1.2 | 2.00 | 0.96 | 208 | 321,634 |
| 2020-03-01 | 1 | 130 | 2 | 514,615 | 2.6 | 1.54 | 0.98 | 204 | 327,941 |
| 2020-03-02 | 2 | 191 | 3 | 350,261 | 1.8 | 1.57 | 0.46 | 649 | 103,002 |
| 2020-03-03 | 3 | 204 | 4 | 327,941 | 10.5 | 1.96 | 1.00 | 401 | 166,694 |
| 2020-03-04 | 4 | 288 | 4 | 232,291 | 2.0 | 1.39 | 0.96 | 416 | 160,624 |
| 2020-03-05 | 5 | 380 | 6 | 176,052 | 2.5 | 1.58 | 1.02 | 586 | 114,124 |
| 2020-03-06 | 6 | 656 | 9 | 101,981 | 1.3 | 1.37 | 0.95 | 945 | 70,737 |
| 2020-03-07 | 7 | 957 | 11 | 69,905 | 1.8 | 1.15 | 0.74 | 1,494 | 44,769 |
| 2020-03-08 | 8 | 1,134 | 19 | 58,994 | 4.1 | 1.68 | 0.56 | 3,415 | 19,586 |
| 2020-03-09 | 9 | 1,217 | 19 | 54,971 | 9.8 | 1.56 | 0.51 | 3,740 | 17,884 |
| 2020-03-10 | 10 | 1,792 | 33 | 37,332 | 1.8 | 1.84 | 0.46 | 7,252 | 9,224 |
| 2020-03-11 | 11 | 2,290 | 48 | 29,213 | 2.8 | 2.10 | 0.65 | 7,431 | 9,002 |
| 2020-03-12 | 12 | 2,290 | 48 | 29,213 | -  | 2.10 | 0.54 | 8,890 | 7,525 |
| 2020-03-13 | 13 | 3,678 | 79 | 18,189 | 1.5 | 2.15 | 0.62 | 12,687 | 5,272 |
| 2020-03-14 | 14 | 4,487 | 91 | 14,909 | 3.5 | 2.03 | 0.57 | 15,828 | 4,226 |
| 2020-03-15 | 15 | 4,523 | 91 | 14,791 | 86.7 | 2.01 | 0.64 | 14,284 | 4,683 |
| 2020-03-16 | 16 | 6,668 | 148 | 10,032 | 1.8 | 2.22 | 0.62 | 23,683 | 2,824 |
| 2020-03-17 | 17 | 7,699 | 148 | 8,689 | 4.8 | 1.92 | 0.68 | 21,649 | 3,090 |
| 2020-03-18 | 18 | 9,105 | 148 | 7,347 | 4.1 | 1.63 | 0.71 | 20,881 | 3,203 |
| 2020-03-19 | 19 | 10,947 | 243 | 6,111 | 3.8 | 2.22 | 0.72 | 33,808 | 1,978 |
| 2020-03-20 | 20 | 12,726 | 450 | 5,256 | 4.6 | 3.54 | 0.77 | 58,162 | 1,150 |
| 2020-03-21 | 21 | 14,431 | 562 | 4,635 | 5.5 | 3.89 | 0.84 | 67,005 | 998 |

## Germany Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -9 | 16 | 0 | 5.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-22 | -8 | 16 | 0 | 5.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-23 | -7 | 16 | 0 | 5.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-24 | -6 | 16 | 0 | 5.2e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-25 | -5 | 17 | 0 | 4.9e6 | 11.4 | 0.00 | 0.00 | - | - |
| 2020-02-26 | -4 | 27 | 0 | 3.1e6 | 1.5 | 0.00 | 0.00 | - | - |
| 2020-02-27 | -3 | 46 | 0 | 1.8e6 | 1.3 | 0.00 | 0.00 | - | - |
| 2020-02-28 | -2 | 48 | 0 | 1.7e6 | 16.3 | 0.00 | 0.00 | - | - |
| 2020-02-29 | -1 | 79 | 0 | 1.0e6 | 1.4 | 0.00 | 0.00 | - | - |
| 2020-03-01 | 0 | 130 | 0 | 637,923 | 1.4 | 0.00 | 0.96 | - | - |
| 2020-03-02 | 1 | 159 | 0 | 521,572 | 3.4 | 0.00 | 0.98 | - | - |
| 2020-03-03 | 2 | 196 | 0 | 423,112 | 3.3 | 0.00 | 0.46 | - | - |
| 2020-03-04 | 3 | 262 | 0 | 316,526 | 2.4 | 0.00 | 1.00 | - | - |
| 2020-03-05 | 4 | 482 | 0 | 172,053 | 1.1 | 0.00 | 0.96 | - | - |
| 2020-03-06 | 5 | 670 | 0 | 123,776 | 2.1 | 0.00 | 1.02 | - | - |
| 2020-03-07 | 6 | 799 | 0 | 103,792 | 3.9 | 0.00 | 0.95 | - | - |
| 2020-03-08 | 7 | 1,040 | 0 | 79,740 | 2.6 | 0.00 | 0.74 | - | - |
| 2020-03-09 | 8 | 1,176 | 2 | 70,518 | 5.6 | 0.17 | 0.56 | - | - |
| 2020-03-10 | 9 | 1,457 | 2 | 56,918 | 3.2 | 0.14 | 0.51 | - | - |
| 2020-03-11 | 10 | 1,908 | 3 | 43,464 | 2.6 | 0.16 | 0.46 | - | - |
| 2020-03-12 | 11 | 2,078 | 3 | 39,908 | 8.1 | 0.14 | 0.65 | - | - |
| 2020-03-13 | 12 | 3,675 | 7 | 22,565 | 1.2 | 0.19 | 0.54 | - | - |
| 2020-03-14 | 13 | 4,585 | 9 | 18,087 | 3.1 | 0.20 | 0.62 | - | - |
| 2020-03-15 | 14 | 5,795 | 11 | 14,310 | 3.0 | 0.19 | 0.57 | - | - |
| 2020-03-16 | 15 | 7,272 | 17 | 11,404 | 3.1 | 0.23 | 0.64 | - | - |
| 2020-03-17 | 16 | 9,257 | 24 | 8,958 | 2.9 | 0.26 | 0.62 | - | - |
| 2020-03-18 | 17 | 12,327 | 28 | 6,727 | 2.4 | 0.23 | 0.68 | - | - |
| 2020-03-19 | 18 | 15,320 | 44 | 5,413 | 3.2 | 0.29 | 0.71 | - | - |
| 2020-03-20 | 19 | 19,848 | 67 | 4,178 | 2.7 | 0.34 | 0.72 | - | - |
| 2020-03-21 | 20 | 22,213 | 84 | 3,733 | 6.2 | 0.38 | 0.77 | - | - |

## India Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -22 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-22 | -21 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-23 | -20 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-24 | -19 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-25 | -18 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-26 | -17 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-27 | -16 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-28 | -15 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-02-29 | -14 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-01 | -13 | 3 | 0 | 450.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-02 | -12 | 5 | 0 | 270.0e6 | 1.4 | 0.00 | 0.00 | - | - |
| 2020-03-03 | -11 | 5 | 0 | 270.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-04 | -10 | 28 | 0 | 48.2e6 | 0.4 | 0.00 | 0.00 | - | - |
| 2020-03-05 | -9 | 30 | 0 | 45.0e6 | 10.0 | 0.00 | 0.00 | - | - |
| 2020-03-06 | -8 | 31 | 0 | 43.5e6 | 21.1 | 0.00 | 0.00 | - | - |
| 2020-03-07 | -7 | 34 | 0 | 39.7e6 | 7.5 | 0.00 | 0.00 | - | - |
| 2020-03-08 | -6 | 39 | 0 | 34.6e6 | 5.1 | 0.00 | 0.00 | - | - |
| 2020-03-09 | -5 | 43 | 0 | 31.4e6 | 7.1 | 0.00 | 0.00 | - | - |
| 2020-03-10 | -4 | 56 | 0 | 24.1e6 | 2.6 | 0.00 | 0.00 | - | - |
| 2020-03-11 | -3 | 62 | 1 | 21.8e6 | 6.8 | 1.61 | 0.00 | - | - |
| 2020-03-12 | -2 | 73 | 1 | 18.5e6 | 4.2 | 1.37 | 0.00 | - | - |
| 2020-03-13 | -1 | 82 | 2 | 16.5e6 | 6.0 | 2.44 | 0.00 | - | - |
| 2020-03-14 | 0 | 102 | 2 | 13.2e6 | 3.2 | 1.96 | 0.96 | 208 | 6.5e6 |
| 2020-03-15 | 1 | 113 | 2 | 11.9e6 | 6.8 | 1.77 | 0.98 | 204 | 6.6e6 |
| 2020-03-16 | 2 | 119 | 2 | 11.3e6 | 13.4 | 1.68 | 0.46 | 433 | 3.1e6 |
| 2020-03-17 | 3 | 142 | 3 | 9.5e6 | 3.9 | 2.11 | 1.00 | 301 | 4.5e6 |
| 2020-03-18 | 4 | 156 | 3 | 8.7e6 | 7.4 | 1.92 | 0.96 | 312 | 4.3e6 |
| 2020-03-19 | 5 | 194 | 4 | 7.0e6 | 3.2 | 2.06 | 1.02 | 390 | 3.5e6 |
| 2020-03-20 | 6 | 244 | 5 | 5.5e6 | 3.0 | 2.05 | 0.95 | 525 | 2.6e6 |
| 2020-03-21 | 7 | 330 | 4 | 4.1e6 | 2.3 | 1.21 | 0.74 | 543 | 2.5e6 |

## Japan Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | 0 | 105 | 1 | 1.2e6 | 6.3 | 0.95 | 0.96 | - | - |
| 2020-02-22 | 1 | 122 | 1 | 1.0e6 | 4.6 | 0.82 | 0.98 | - | - |
| 2020-02-23 | 2 | 147 | 1 | 862,517 | 3.7 | 0.68 | 0.46 | 216 | 585,635 |
| 2020-02-24 | 3 | 159 | 1 | 797,421 | 8.8 | 0.63 | 1.00 | - | - |
| 2020-02-25 | 4 | 170 | 1 | 745,823 | 10.4 | 0.59 | 0.96 | - | - |
| 2020-02-26 | 5 | 189 | 2 | 670,846 | 6.5 | 1.06 | 1.02 | 195 | 648,874 |
| 2020-02-27 | 6 | 214 | 4 | 592,476 | 5.6 | 1.87 | 0.95 | 420 | 301,641 |
| 2020-02-28 | 7 | 228 | 4 | 556,096 | 10.9 | 1.75 | 0.74 | 543 | 233,333 |
| 2020-02-29 | 8 | 241 | 5 | 526,099 | 12.5 | 2.07 | 0.56 | 898 | 141,058 |
| 2020-03-01 | 9 | 256 | 6 | 495,273 | 11.5 | 2.34 | 0.51 | 1,181 | 107,335 |
| 2020-03-02 | 10 | 274 | 6 | 462,737 | 10.2 | 2.19 | 0.46 | 1,318 | 96,155 |
| 2020-03-03 | 11 | 293 | 6 | 432,730 | 10.3 | 2.05 | 0.65 | 928 | 136,490 |
| 2020-03-04 | 12 | 331 | 6 | 383,051 | 5.7 | 1.81 | 0.54 | 1,111 | 114,093 |
| 2020-03-05 | 13 | 360 | 6 | 352,194 | 8.3 | 1.67 | 0.62 | 963 | 131,579 |
| 2020-03-06 | 14 | 420 | 6 | 301,880 | 4.5 | 1.43 | 0.57 | 1,043 | 121,486 |
| 2020-03-07 | 15 | 461 | 6 | 275,032 | 7.4 | 1.30 | 0.64 | 941 | 134,617 |
| 2020-03-08 | 16 | 502 | 6 | 252,569 | 8.1 | 1.20 | 0.62 | 960 | 132,054 |
| 2020-03-09 | 17 | 511 | 10 | 248,121 | 39.0 | 1.96 | 0.68 | 1,462 | 86,676 |
| 2020-03-10 | 18 | 581 | 10 | 218,227 | 5.4 | 1.72 | 0.71 | 1,410 | 89,861 |
| 2020-03-11 | 19 | 639 | 15 | 198,419 | 7.3 | 2.35 | 0.72 | 2,086 | 60,753 |
| 2020-03-12 | 20 | 639 | 16 | 198,419 | -  | 2.50 | 0.77 | 2,068 | 61,310 |
| 2020-03-13 | 21 | 701 | 19 | 180,870 | 7.5 | 2.71 | 0.84 | 2,265 | 55,970 |
| 2020-03-14 | 22 | 773 | 22 | 164,023 | 7.1 | 2.85 | 0.83 | 2,659 | 47,671 |
| 2020-03-15 | 23 | 839 | 22 | 151,120 | 8.5 | 2.62 | 0.89 | 2,470 | 51,316 |
| 2020-03-16 | 24 | 825 | 27 | 153,684 | -  | 3.27 | 0.92 | 2,938 | 43,150 |
| 2020-03-17 | 25 | 878 | 29 | 144,407 | 11.1 | 3.30 | 0.91 | 3,184 | 39,813 |
| 2020-03-18 | 26 | 889 | 29 | 142,620 | 55.7 | 3.26 | 0.97 | 2,978 | 42,564 |
| 2020-03-19 | 27 | 924 | 29 | 137,218 | 18.0 | 3.14 | 1.00 | 2,904 | 43,653 |
| 2020-03-20 | 28 | 963 | 33 | 131,661 | 16.8 | 3.43 | 1.06 | 3,105 | 40,821 |
| 2020-03-21 | 29 | 1,007 | 35 | 125,908 | 15.5 | 3.48 | 1.09 | 3,221 | 39,357 |

## Ecuador Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -26 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-22 | -25 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-23 | -24 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-24 | -23 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-25 | -22 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-26 | -21 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-27 | -20 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-28 | -19 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-02-29 | -18 | 0 | 0 | - | -  | 0.00 | 0.00 | - | - |
| 2020-03-01 | -17 | 6 | 0 | 2.8e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-02 | -16 | 6 | 0 | 2.8e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-03 | -15 | 7 | 0 | 2.4e6 | 4.5 | 0.00 | 0.00 | - | - |
| 2020-03-04 | -14 | 10 | 0 | 1.7e6 | 1.9 | 0.00 | 0.00 | - | - |
| 2020-03-05 | -13 | 13 | 0 | 1.3e6 | 2.6 | 0.00 | 0.00 | - | - |
| 2020-03-06 | -12 | 13 | 0 | 1.3e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-07 | -11 | 13 | 0 | 1.3e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-08 | -10 | 14 | 0 | 1.2e6 | 9.4 | 0.00 | 0.00 | - | - |
| 2020-03-09 | -9 | 15 | 0 | 1.1e6 | 10.0 | 0.00 | 0.00 | - | - |
| 2020-03-10 | -8 | 15 | 0 | 1.1e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-11 | -7 | 17 | 0 | 1.0e6 | 5.5 | 0.00 | 0.00 | - | - |
| 2020-03-12 | -6 | 17 | 0 | 1.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-13 | -5 | 17 | 0 | 1.0e6 | -  | 0.00 | 0.00 | - | - |
| 2020-03-14 | -4 | 28 | 2 | 610,000 | 1.4 | 7.14 | 0.00 | - | - |
| 2020-03-15 | -3 | 28 | 2 | 610,000 | -  | 7.14 | 0.00 | - | - |
| 2020-03-16 | -2 | 37 | 2 | 461,621 | 2.5 | 5.41 | 0.00 | - | - |
| 2020-03-17 | -1 | 58 | 2 | 294,482 | 1.5 | 3.45 | 0.00 | - | - |
| 2020-03-18 | 0 | 111 | 2 | 153,873 | 1.1 | 1.80 | 0.96 | 208 | 82,115 |
| 2020-03-19 | 1 | 199 | 3 | 85,829 | 1.2 | 1.51 | 0.98 | 306 | 55,816 |
| 2020-03-20 | 2 | 367 | 5 | 46,539 | 1.1 | 1.36 | 0.46 | 1,082 | 15,778 |
| 2020-03-21 | 3 | 506 | 7 | 33,754 | 2.2 | 1.38 | 1.00 | 702 | 24,318 |

## Canada Cases (Reported and Inferred)

| Date | Dn  | Confirmed | Deaths | Pop/Confirmed | Doubling | Deaths (%) | KR Deaths (%) | Inferred Cases | Pop/Inferred |
|:----:|:---:|:---------:|:------:|:-------------:|:--------:|:-----------:|:--------------:|:---------------:|:----------:|
| 2020-02-21 | -19 | 9 | 0 | 419,972 | 5.9 | 0.00 | 0.00 | - | - |
| 2020-02-22 | -18 | 9 | 0 | 419,972 | -  | 0.00 | 0.00 | - | - |
| 2020-02-23 | -17 | 9 | 0 | 419,972 | -  | 0.00 | 0.00 | - | - |
| 2020-02-24 | -16 | 10 | 0 | 377,974 | 6.6 | 0.00 | 0.00 | - | - |
| 2020-02-25 | -15 | 11 | 0 | 343,613 | 7.3 | 0.00 | 0.00 | - | - |
| 2020-02-26 | -14 | 11 | 0 | 343,613 | -  | 0.00 | 0.00 | - | - |
| 2020-02-27 | -13 | 13 | 0 | 290,749 | 4.1 | 0.00 | 0.00 | - | - |
| 2020-02-28 | -12 | 14 | 0 | 269,982 | 9.4 | 0.00 | 0.00 | - | - |
| 2020-02-29 | -11 | 20 | 0 | 188,987 | 1.9 | 0.00 | 0.00 | - | - |
| 2020-03-01 | -10 | 24 | 0 | 157,489 | 3.8 | 0.00 | 0.00 | - | - |
| 2020-03-02 | -9 | 27 | 0 | 139,990 | 5.9 | 0.00 | 0.00 | - | - |
| 2020-03-03 | -8 | 30 | 0 | 125,991 | 6.6 | 0.00 | 0.00 | - | - |
| 2020-03-04 | -7 | 33 | 0 | 114,537 | 7.3 | 0.00 | 0.00 | - | - |
| 2020-03-05 | -6 | 37 | 0 | 102,155 | 6.1 | 0.00 | 0.00 | - | - |
| 2020-03-06 | -5 | 49 | 0 | 77,137 | 2.5 | 0.00 | 0.00 | - | - |
| 2020-03-07 | -4 | 54 | 0 | 69,995 | 7.1 | 0.00 | 0.00 | - | - |
| 2020-03-08 | -3 | 64 | 0 | 59,058 | 4.1 | 0.00 | 0.00 | - | - |
| 2020-03-09 | -2 | 77 | 1 | 49,087 | 3.7 | 1.30 | 0.00 | - | - |
| 2020-03-10 | -1 | 79 | 1 | 47,844 | 27.0 | 1.27 | 0.00 | - | - |
| 2020-03-11 | 0 | 108 | 1 | 34,997 | 2.2 | 0.93 | 0.96 | - | - |
| 2020-03-12 | 1 | 117 | 1 | 32,305 | 8.7 | 0.85 | 0.98 | - | - |
| 2020-03-13 | 2 | 193 | 1 | 19,584 | 1.4 | 0.52 | 0.46 | 216 | 17,458 |
| 2020-03-14 | 3 | 198 | 1 | 19,089 | 27.1 | 0.51 | 1.00 | - | - |
| 2020-03-15 | 4 | 252 | 1 | 14,999 | 2.9 | 0.40 | 0.96 | - | - |
| 2020-03-16 | 5 | 415 | 4 | 9,107 | 1.4 | 0.96 | 1.02 | - | - |
| 2020-03-17 | 6 | 478 | 5 | 7,907 | 4.9 | 1.05 | 0.95 | 525 | 7,193 |
| 2020-03-18 | 7 | 657 | 8 | 5,753 | 2.2 | 1.22 | 0.74 | 1,086 | 3,477 |
| 2020-03-19 | 8 | 800 | 9 | 4,724 | 3.5 | 1.13 | 0.56 | 1,617 | 2,336 |
| 2020-03-20 | 9 | 943 | 12 | 4,008 | 4.2 | 1.27 | 0.51 | 2,362 | 1,599 |
| 2020-03-21 | 10 | 1,278 | 19 | 2,957 | 2.3 | 1.49 | 0.46 | 4,175 | 905 |

## World cases (outside China)

|  Date  |  Confirmed |  Deaths | Rate (%) | KR Normalized | Doubling Days |
|:------:|:----------:|:-------:|:---------:|:-------------:|:-------------:|
| 2020-02-21 | 1,273 | 13 | 1.02 | 1,121 | 5.4 |
| 2020-02-22 | 1,578 | 15 | 0.95 | 1,293 | 3.2 |
| 2020-02-23 | 1,943 | 24 | 1.24 | 2,070 | 3.3 |
| 2020-02-24 | 2,327 | 34 | 1.46 | 2,933 | 3.8 |
| 2020-02-25 | 2,659 | 43 | 1.62 | 3,709 | 5.2 |
| 2020-02-26 | 3,229 | 53 | 1.64 | 4,572 | 3.6 |
| 2020-02-27 | 4,154 | 68 | 1.64 | 5,866 | 2.8 |
| 2020-02-28 | 5,192 | 82 | 1.58 | 7,073 | 3.1 |
| 2020-02-29 | 6,655 | 104 | 1.56 | 8,971 | 2.8 |
| 2020-03-01 | 8,437 | 124 | 1.47 | 10,696 | 2.9 |
| 2020-03-02 | 10,170 | 171 | 1.68 | 14,751 | 3.7 |
| 2020-03-03 | 12,579 | 213 | 1.69 | 18,374 | 3.3 |
| 2020-03-04 | 14,734 | 271 | 1.84 | 23,377 | 4.4 |
| 2020-03-05 | 17,345 | 333 | 1.92 | 28,726 | 4.2 |
| 2020-03-06 | 21,094 | 416 | 1.97 | 35,886 | 3.5 |
| 2020-03-07 | 25,051 | 486 | 1.94 | 41,924 | 4.0 |
| 2020-03-08 | 28,972 | 702 | 2.42 | 60,557 | 4.8 |
| 2020-03-09 | 32,701 | 865 | 2.65 | 74,618 | 5.7 |
| 2020-03-10 | 37,541 | 1,123 | 2.99 | 96,875 | 5.0 |
| 2020-03-11 | 44,772 | 1,454 | 3.25 | 125,428 | 3.9 |
| 2020-03-12 | 47,226 | 1,548 | 3.28 | 133,537 | 13.0 |
| 2020-03-13 | 64,048 | 2,224 | 3.47 | 191,852 | 2.3 |
| 2020-03-14 | 74,902 | 2,626 | 3.51 | 226,531 | 4.4 |
| 2020-03-15 | 86,196 | 3,237 | 3.76 | 279,238 | 4.9 |
| 2020-03-16 | 100,208 | 3,909 | 3.90 | 337,208 | 4.6 |
| 2020-03-17 | 115,776 | 4,675 | 4.04 | 403,287 | 4.8 |
| 2020-03-18 | 133,491 | 5,492 | 4.11 | 473,765 | 4.9 |
| 2020-03-19 | 161,115 | 6,618 | 4.11 | 570,899 | 3.7 |
| 2020-03-20 | 190,360 | 8,044 | 4.23 | 693,913 | 4.2 |
| 2020-03-21 | 222,545 | 9,712 | 4.36 | 837,802 | 4.4 |

Mean doubling days for last 30 days: 4.3