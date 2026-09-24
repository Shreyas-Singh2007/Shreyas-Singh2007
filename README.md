# Multi-Threaded CSV File Processor

A beginner-level Java project that reads multiple CSV files at the same time using threads, and produces a combined sales report.

---

## What This Project Does

- Reads 3 CSV sales files **at the same time** (using multiple threads)
- Uses a **Builder Pattern** to set up configuration
- Combines all data and prints a **Sales Report**
- Saves the report to `report.txt`


============================================
  Multi-Threaded CSV File Processor
============================================

Configuration: ProcessorConfig{threads=3, inputFolder='data/', ...}

Found 3 CSV file(s) to process:

  -> sales_february.csv
  -> sales_january.csv
  -> sales_march.csv

Processing files concurrently...

[Thread: pool-1-thread-1] Processing: data\sales_february.csv
[Thread: pool-1-thread-2] Processing: data\sales_january.csv
[Thread: pool-1-thread-3] Processing: data\sales_march.csv
[Thread: pool-1-thread-2] Done! Parsed 8 records from: data\sales_january.csv
[Thread: pool-1-thread-3] Done! Parsed 9 records from: data\sales_march.csv
[Thread: pool-1-thread-1] Done! Parsed 8 records from: data\sales_february.csv

All threads finished. Thread pool shut down.

=======================================================
       SALES AGGREGATED REPORT
=======================================================

  Total Records Processed : 25
  Total Quantity Sold     : 915 units
  Total Revenue           : $57,650.85
  ...

Report saved to: report.txt
