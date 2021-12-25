The [intl package](https://pub.dev/packages/intl) supports a broad range of date formatting patterns. Here's a list (taken from [the official docs](https://pub.dev/documentation/intl/latest/intl/DateFormat-class.html)):

1.  DAY                          d
2.   ABBR_WEEKDAY                 E
3.   WEEKDAY                      EEEE
4.   ABBR_STANDALONE_MONTH        LLL
5.   STANDALONE_MONTH             LLLL
6.   NUM_MONTH                    M
7.   NUM_MONTH_DAY Md
8.   NUM_MONTH_WEEKDAY_DAY MEd
9.   ABBR_MONTH                   MMM
10.   ABBR_MONTH_DAY MMMd
11.   ABBR_MONTH_WEEKDAY_DAY MMMEd
12.   MONTH                        MMMM
13.   MONTH_DAY MMMMd
14.   MONTH_WEEKDAY_DAY MMMMEEEEd
15.   ABBR_QUARTER                 QQQ
16.   QUARTER                      QQQQ
17.   YEAR                         y
18.   YEAR_NUM_MONTH               yM
19.   YEAR_NUM_MONTH_DAY           yMd
20.   YEAR_NUM_MONTH_WEEKDAY_DAY   yMEd
21.   YEAR_ABBR_MONTH              yMMM
22.   YEAR_ABBR_MONTH_DAY          yMMMd
23.   YEAR_ABBR_MONTH_WEEKDAY_DAY  yMMMEd
24.   YEAR_MONTH                   yMMMM
25.   YEAR_MONTH_DAY               yMMMMd
26.   YEAR_MONTH_WEEKDAY_DAY       yMMMMEEEEd
27.   YEAR_ABBR_QUARTER            yQQQ
28.   YEAR_QUARTER                 yQQQQ
29.   HOUR24                       H
30.   HOUR24_MINUTE Hm
31.   HOUR24_MINUTE_SECOND Hms
32.   HOUR                         j
33.   HOUR_MINUTE                  jm
34.   HOUR_MINUTE_SECOND           jms
35.   HOUR_MINUTE_GENERIC_TZ       jmv
36.   HOUR_MINUTE_TZ               jmz
37.   HOUR_GENERIC_TZ              jv
38.   HOUR_TZ                      jz
39.   MINUTE                       m
40.   MINUTE_SECOND                ms
41.   SECOND                       s

Examples Using the US Locale:

1.   Pattern Result
2.   ---------------- -------
3.   new DateFormat.yMd() -> 7/10/1996
4.   new DateFormat("yMd") -> 7/10/1996
5.   new DateFormat.yMMMMd("en_US") -> July 10, 1996
6.   new DateFormat.jm() -> 5:08 PM
7.   new DateFormat.yMd().add_jm() -> 7/10/1996 5:08 PM
8.   new DateFormat.Hm() -> 17:08 // force 24 hour time