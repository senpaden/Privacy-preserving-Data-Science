# Presentation Slide PDF (without animation effects): 

[https://drive.google.com/file/d/1PUYqaUE64Obi3mcRvlwEkQ7RgDWV0twP/view?usp=sharing](https://drive.google.com/file/d/1ZxkEDyDkoyJVmAn3ONCLZA-1hp4RZv1E/view?usp=sharing)

# Privacy-preserving Data Science  
*Mitigating Execution Time Leakage in Differential Privacy*

This repository contains code and materials for implementing privacy-preserving data analysis techniques using differential privacy in a database context. The project focuses on reducing execution time leakage in private SQL query processing by applying padding techniques, allowing tunable trade-offs between privacy and utility.

## Overview

The project integrates OpenDP with PostgreSQL to enable privacy-safe data queries on cloud databases. It demonstrates methods to:

- Protect query execution time to minimize side-channel attacks.
- Implement padding techniques that balance privacy guarantees and query performance.
- Visualize and evaluate privacy-utility trade-offs.
  
## Background

- Conventional data privacy methods have significant limitations and assumptions.  
- Differential Privacy improves privacy guarantees by protecting individuals and adding controlled noise.  
- However, it is vulnerable to execution time leakage attacks, which this project aims to mitigate.

## Proposed Solutions

- **Manual Time Delay:** Introduces fixed delays but is largely ineffective in practice.  
- **Data Padding:** Adds dummy data to mask query sizes and execution times.  
  - **Full Padding:** Offers strong privacy by fully hiding execution time patterns but at the cost of reduced utility and slower runtimes.  
  - **Partial Padding (Differential Privacy Padding):** Provides a balanced trade-off, improving efficiency while still protecting user-decided privacy.
    
## Features

- Padding strategies to reduce timing leakage in differential privacy.
- Integration of PostgreSQL with Python for executing and managing private queries.
- Visualization of query performance and padding effectiveness using R.
- Reproducible Jupyter notebooks and scripts for experimentation.

## Requirements

- Python 3.x
- PostgreSQL
- R (for visualization)
- Python libraries: `opendp`, `psycopg2`, `pandas`, `matplotlib`
- R packages: `ggplot2`

## Installation

1. Set up PostgreSQL and create a test database.
2. Install Python dependencies:  

   pip install opendp psycopg2 pandas matplotlib
   
## Usage

1. Configure database connection parameters in the scripts.  
2. Run Python scripts to execute private queries with padding.  
3. Use the R scripts/notebooks to visualize performance and privacy trade-offs.

## Key Scripts (private)

- `padding_techniques.py`: Implements padding methods to mask execution time.  
- `query_runner.py`: Executes private SQL queries using OpenDP and padding.  
- `visualize_performance.R`: R script to generate performance plots.  

## Results

The padding technique reduced query slowdown from 93–1054× to 54–471× while maintaining tunable privacy-utility trade-offs, demonstrating significant performance improvement in privacy-preserving queries.
