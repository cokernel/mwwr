mwwr
====

This program computes the Hodges--Lehmann estimator for two samples,
performs the Mann--Whitney--Wilcoxon test on the samples, and generates
a report of the results.

The program assumes that each sample contains more than 20 data points.

Sample report:

```
Summary of dh.a.sc: n = 389.0, median = 5077.0 [q1 = 4258.0, q3 = 5651.0] (min = 1019.0, max = 8196.0)
Summary of dh.b.sc: n = 24.0, median = 4426.5 [q1 = 4264.5, q3 = 4691.5] (min = 3668.0, max = 5252.0)
Hodges-Lehmann estimator (median {dh.b.sc - dh.a.sc}) = -630.5

Null hypothesis:
H0 = The distributions of dh.a.sc and dh.b.sc do not significantly differ.
U-statistic for dh.a.sc.txt: 6463.5
U-statistic for dh.b.sc.txt: 2872.5
U-statistic (minimum): 2872.5
Z-score: -3.1637052395040945
|-3.1637052395040945| >= 1.96, so we reject the null hypothesis.
```

Usage
-----

Install the programs on your PATH.

Select a prefix for your sample filenames, e.g., $cond.

Store your first sample in $cond.a.txt and your second sample in $cond.b.txt .  Each file
should have one numeric or ordinal data point per line.  The samples do not need to be
sorted.

To generate the report:

```
mwwr $cond
```

This generates the file $cond.report.txt and various intermediate files.  If you do not
wish to keep the intermediate files, you can remove them with the command

```
mwwr-cleanup $cond
```

This command does not remove the report.

License
-------

Copyright (c) 2018 Michael Slone.

See LICENSE for terms.
