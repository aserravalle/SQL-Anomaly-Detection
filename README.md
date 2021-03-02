# SQL-Anomaly-Detection

anomaly_detection.sql can convert this:

StockData
=====================================
`Ticker     Period   Price
---------- -------- -------------
stock1     2020-03  13.00
stock2     2020-03  7.00
stock3     2020-05  38272.00
stock4     2020-05  1.00
stock5     2020-08  83.00`
 
 To this:
 
 TimeSeriesGrouped:
 ==========================================
`Ticker      Period   Price  PctChange  IsPctAnomaly  IsQuartileAnomaly  IsPercentileAnomaly
------------ -------- ------ ---------- ------------- ------------------ ----------------
stock7       2019-08  1.00   NULL       0             0                  1
stock7       2020-02  1.00   NULL       0             0                  1
stock7       2020-03  5.00   4.0000     0             0                  0
stock7       2020-04  2.00   -0.6000    0             0                  0
stock7       2020-05  33.00  15.5000    1             0                  0
stock7       2020-06  9.00   -0.7273    0             0                  0
stock7       2020-07  362.00 39.2222    1             1                  0
stock7       2020-08  32.00  -0.9116    1             0                  0
stock7       2020-09  93.00  1.9063     0             1                  0`
