---
layout: page
title: Access TravisTorrent
subtitle: Free and Open Travis Analytics for Everyone
comments: true
---

As a courtesy to our users, TravisTorrent provides both offline and online
access options. No registration or subscription is required. Users are kindly asked to follow a fair-use policy of server resources.

<div class="get-started-wrap"><a class="btn btn-success btn-lg get-started-btn" href="https://bigquery.cloud.google.com/table/travistorrent-bq:data.2017_02_08?tab=schema">Live Online Access</a> <a class="btn btn-success btn-lg get-started-btn" href="/dumps/travistorrent_8_2_2017.sql.gz">Download CSV dump</a> (live access is currently no longer possible, see **offline access** below to continue).</div>
<br>

### Live Online Access
Thanks to Google, we can [provide a BigQuery interface](https://bigquery.cloud.google.com/table/travistorrent-bq:data.2017_01_11?tab=schema) to TravisTorrent. Everyone with a Google account gets a free monthly quota of one Terabyte on BigQuery to instantly start querying TravisTorrent!

Usage Instructions:  If you are not fully signed-up for Big Query (you get an error saying Big Query is unable to find the TravisTorrent table when clicking the access link), follow [Google's instructions on how to set it up.](https://cloud.google.com/blog/big-data/2017/01/how-to-run-a-terabyte-of-google-bigquery-queries-each-month-without-a-credit-card) Should you not already be in the query browser, click on the big red button on the top left that says `Compose Query`. You can then input sample queries in SQL syntax and run them via `CTRL+ENTER`.  For example, ``SELECT AVG(tr_duration) FROM [travistorrent-bq:data.2017_01_11]`` computes the average mean build time over all projects. 

### Offline Access
**Update March 7, 2022: The links in the table below no longer work and is kept in-place only for archival purposes. Please download the [TravisTorrent dump from Figshare,](https://doi.org/10.6084/m9.figshare.19314170) where it should be kept "forever".**

We distribute snapshots of our database as compressed SQL and CSV files. The SQL is generated from automatically reading in the CSV.

Tip: If you use R and CSV, loading the CSV via `fread` from `data.table` offers a significant speed-up over `read.csv`.

|Snapshot Revision|Date|Size|
|[travistorrent_8_2_2017.csv.gz](/dumps/travistorrent_8_2_2017.csv.gz)|11.1.2017|184M|
|[travistorrent_8_2_2017.sql.gz](/dumps/travistorrent_8_2_2017.sql.gz)|11.1.2017|181M|
|archived: [travistorrent_11_1_2017.csv.gz](/dumps/travistorrent_11_1_2017.csv.gz)|11.1.2017|190M|
|archived: [travistorrent_11_1_2017.sql.gz](/dumps/travistorrent_11_1_2017.sql.gz)|11.1.2017|193M|
|archived: [travistorrent_6_12_2016.sql.gz](/dumps/travistorrent_6_12_2016.sql.gz)|6.12.2016|178M|
|archived: [travistorrent_6_12_2016.csv.gz](/dumps/travistorrent_6_12_2016.csv.gz)|6.12.2016|175M|
|archived: [travistorrent_27_10_2016.sql.gz](/dumps/travistorrent_27_10_2016.sql.gz)|27.10.2016|78M|
|archived: [travistorrent_27_10_2016.csv.gz](/dumps/travistorrent_27_10_2016.csv.gz)|27.10.2016|78M|
|archived: [travistorrent_30_9_2016.sql.gz](/dumps/travistorrent_30_9_2016.sql.gz)|30.9.2016|78M|
|archived: [travistorrent_30_9_2016.csv.gz](/dumps/travistorrent_30_9_2016.csv.gz) <br><sub>Includes changes to data types, e.g. TRUE instead of "true"</sub>|30.9.2016|79M|
|archived: [travistorrent_7_9_2016.sql.gz](/dumps/travistorrent_7_9_2016.sql.gz)|7.9.2016|78M|
|archived: [travistorrent_7_9_2016.csv.gz](/dumps/travistorrent_7_9_2016.csv.gz)|7.9.2016|79M|
|archived: [travistorrent_5_3_2016.sql.gz](/dumps/travistorrent_5_3_2016.sql.gz)|5.3.2016|51M|
|archived: [travistorrent_5_3_2016.csv.gz](/dumps/travistorrent_5_3_2016.csv.gz)|5.3.2016|79M|
|archived: [travistorrent_28_8_2015.csv.gz](/dumps/travistorrent_28_8_2015.csv.gz)|28.8.2015|65M|

### Raw Build Data
**Update March 7, 2022: Access to raw build logs is no longer possible.**

To allow a deeper analysis of project build logs, the 780 GB of build logs that our build log analysis (most entries prefixed with `tr_`) depends on can be retrieved, too. Please be gentle with server bandwidth. [Access the raw build logs](#). If you used these, please also [cite or reference TravisTorrent properly](/#cite).
