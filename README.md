# data-integration-labs
#Title: Ausprobieren Tool 
Es ist zum lernen und ausprobieren für den kurs von DIS.3.3
Name: Muhammed Salih Akpolat 
My own profile: https://github.com/MuhammedSalihAkpolat
to the course respitory: https://github.com/breuert/data-integration
to out tems respitory: https://github.com/Esmaa21/Data-Integration-3.3#
labs/01/
link tpo my lab respitory: https://github.com/MuhammedSalihAkpolat/data-integration-labs

Attempt | #1 | #2 | #3 | #4 | #5 | #6 | #7 | #8 | #9 | #10 | #11
--- | --- | --- | --- |--- |--- |--- |--- |--- |--- |--- |---
Seconds | 301 | 283 | 290 | 286 | 289 | 285 | 287 | 287 | 272 | 276 | 269



Mein Datensett wird sein: https://data.ecb.europa.eu/data/datasets/ICP/ICP.M.U2.N.094210.4.ANR

Task 6:
# Dataset Profile – HICP: Cinemas, theatres and concerts

## Task 6 – Profile the dataset

### 1. Facts

The selected dataset is provided through the European Central Bank (ECB) Data Portal. It contains information about the Harmonised Index of Consumer Prices (HICP) for cinemas, theatres and concerts in the euro area.

The dataset is used to examine the annual price changes in the cultural and entertainment sector.

| Criterion | Description |
|---|---|
| Title | HICP – Cinemas, theatres and concerts |
| Publisher / Data portal | European Central Bank (ECB) |
| Dataset category | Indices of Consumer Prices (ICP) |
| Series identifier | ICP.M.U2.N.094210.4.ANR |
| Data format | CSV (Comma-Separated Values) |
| Frequency | Monthly |
| Geographic coverage | Euro area (U2) |
| Time coverage of downloaded file | December 2017 – December 2025 |
| Number of observations | 97 |
| Number of columns | 3 |
| Measurement unit | Annual percentage change (%) |
| Update frequency | Monthly |
| Data access | Publicly accessible via the ECB Data Portal and API |

The series identifier contains information about the dataset:

- `ICP`: Indices of Consumer Prices
- `M`: Monthly frequency
- `U2`: Euro area
- `N`: Non-seasonally adjusted data
- `094210`: Classification code for cinemas, theatres and concerts
- `4`: Data provider code
- `ANR`: Annual rate of change

The data show how prices have changed compared with the same month of the previous year. They do not represent absolute ticket prices in euros.

**Source:** [ECB Data Portal – HICP dataset](https://data.ecb.europa.eu/data/datasets/ICP/ICP.M.U2.N.094210.4.ANR)

### 2. Stars – Five-star evaluation

The dataset was evaluated using a five-star scheme.

| Criterion | Evaluation | Explanation |
|---|---|---|
| Findability | ★★★★★ | The dataset can be found through the ECB Data Portal using a unique series identifier. |
| Accessibility | ★★★★★ | The data are publicly accessible and can be downloaded in CSV format or retrieved through an API. |
| Interoperability | ★★★★★ | The ECB uses the standardized SDMX data format. |
| Reusability | ★★★★☆ | The data can be reused under the applicable source attribution and reuse conditions. |
| Metadata quality | ★★★★☆ | Important information is available, but additional documentation is needed to understand all variables and codes. |

**Overall rating: 4 out of 5 stars.**

The dataset is easy to find, publicly accessible and available in a machine-readable format. Its standardized structure makes it suitable for further analysis.

However, the documentation of individual variables and the applicable reuse conditions should be examined more closely. Therefore, the dataset does not receive the full five stars.

### 3. Open the data

The downloaded CSV file was examined using Python and the pandas library.

The file contains 97 observations covering the period from December 2017 to December 2025.

#### Structure of the CSV file

| Column | Description | Data type |
|---|---|---|
| DATE | Observation date | Date / String |
| TIME PERIOD | Observation month | String |
| HICP - Cinemas, theatres, concerts (ICP.M.U2.N.094210.4.ANR) | Annual price change | Numeric (Float) |

#### Statistical analysis

The numerical column was examined to calculate the minimum, maximum and mean values.

| Statistical measure | Result |
|---|---:|
| Minimum | -1.0 % |
| Maximum | 5.4 % |
| Mean | 2.39 % |
| Number of observations | 97 |
| Missing values | 0 |

The minimum value of -1.0 % occurred in May 2021.

The maximum value of 5.4 % occurred in August 2023.

The average annual price change across all 97 observations was approximately 2.39 %.

#### Data quality and unusual observations

Several characteristics were identified during the examination:

1. There are no missing values in the three columns.
2. The dataset contains negative values. For example, in May 2021, the annual price change was -1.0 %. This means that prices were lower than in the same month of the previous year.
3. The highest value was recorded in August 2023, with an annual price increase of 5.4 %.
4. The file contains two columns representing time: `DATE` and `TIME PERIOD`. Both refer to the same observation month but use different formats.
5. Decimal values use a dot as the decimal separator.
6. The values represent percentage changes rather than actual ticket prices in euros.

The dataset is therefore suitable for analysing price developments over time. However, it cannot be used to determine the actual price of an individual concert ticket.

**Tool used:** Python with the pandas library.

### 4. Data dictionary

The downloaded CSV file contains three columns. To provide a more complete description, two additional metadata dimensions from the ECB data structure are included below. These two dimensions are not separate columns in the downloaded CSV file.

| Variable | Meaning | Data type | Unit | Example |
|---|---|---|---|---|
| DATE | Date of the observation | Date | Date | 2023-08-31 |
| TIME PERIOD | Month of the observation | String | Month | 2023Aug |
| HICP value | Annual percentage change in prices | Float | Percent (%) | 5.4 |
| FREQ | Observation frequency | Code | None | M |
| REF_AREA | Geographic reference area | Code | None | U2 |

The ECB provides documentation about the data structure and its dimensions through its SDMX documentation.

Documentation: [ECB Data Structure – ICP](https://data.ecb.europa.eu/data/datasets/ICP/structure?showDatasetModal=false)

The documentation helps users understand the meaning of the individual dimensions and codes.

### 5. Licence

The ECB provides publicly released statistics free of charge for reuse, subject to its reuse policy.

The main conditions are:

- The original source must be acknowledged.
- The statistics and metadata must not be modified when reused under the ECB's reuse policy.
- Third-party data may be subject to additional conditions.
- Users should take possible revisions and updates into account.

The data are publicly accessible and can be reused with appropriate attribution. However, the conditions must be considered when modifying or redistributing the dataset.

According to the Open Definition, open data should be freely accessible, reusable and redistributable, including the possibility of making adaptations.

Therefore, the ECB's conditions concerning unmodified statistics must be considered when assessing whether the dataset fully meets the Open Definition.

**TASL attribution for the project README:**

- **Title:** HICP – Cinemas, theatres and concerts
- **Author / Publisher:** European Central Bank (ECB)
- **Source:** [ECB Data Portal](https://data.ecb.europa.eu/data/datasets/ICP/ICP.M.U2.N.094210.4.ANR)
- **Licence / Reuse conditions:** ECB Policy regarding the reuse of ESCB statistics – free reuse with source attribution and subject to the applicable conditions.

Further information:
[ECB – Policy regarding the reuse of statistics](https://www.ecb.europa.eu/stats/ecb_statistics/governance_and_quality_framework/html/usage_policy.de.html)

### 6. People – Personal data

The dataset does not contain personal data.

It consists of aggregated statistical information about price changes in the cultural and entertainment sector.

There are no personal names, addresses, contact details or individual purchase records.

Therefore, no personal identification is possible based on the downloaded dataset.

No anonymization or additional data protection measures are necessary for this dataset.

---

## Task 7 – Review it with the FAIR principles

The dataset was evaluated according to the four FAIR principles: Findable, Accessible, Interoperable and Reusable.

| FAIR principle | Evaluation | Explanation |
|---|---|---|
| Findable | Fulfilled | The dataset has a unique identifier and can be found through the ECB Data Portal. |
| Accessible | Fulfilled | The data can be accessed publicly through the ECB website and its API. |
| Interoperable | Fulfilled | The ECB uses the standardized SDMX format, which supports data exchange between different systems. |
| Reusable | Partially fulfilled | The dataset can be reused with source attribution, but the applicable reuse conditions and metadata must be considered. |

### Findable

The dataset is easy to find through the ECB Data Portal. Its unique series identifier allows users to locate the exact data series.

### Accessible

The dataset is publicly available and can be downloaded in CSV format. It can also be retrieved through the ECB's SDMX API.

### Interoperable

The dataset uses the SDMX standard, which is widely used for exchanging statistical data. This makes it possible to process the data with different software applications.

### Reusable

The dataset can be reused for further statistical analysis if the applicable source attribution and reuse conditions are respected. The documentation also provides information about the data structure and measurement units.

### Overall FAIR assessment

The dataset largely fulfils the FAIR principles. Its main strengths are its public accessibility, unique identifier and standardized data structure.

Some limitations remain regarding the documentation and the conditions for reuse. These aspects should be considered when using the dataset in other projects.

Overall, the dataset is suitable for further statistical analysis and for examining price developments in the cultural and entertainment sector.


## Task 7 – Review the dataset with the FAIR principles

The dataset was checked using the FAIR principles. The following table shows the results.

| Principle | Rating | Explanation |
|---|:---:|---|
| F1 | ✓ | The dataset has a unique series ID and a stable URL on the ECB website. |
| F2 | ~ | Important information such as title, publisher and description is available, but some metadata is missing. |
| F4 | ✓ | The dataset can easily be found through the ECB Data Portal. |
| A1 | ✓ | The data can be downloaded via HTTPS or the ECB API without logging in. |
| I1 | ✓ | The dataset is available as a CSV file and can be opened with Excel or LibreOffice. |
| I2, I3 | ✓ | Standard codes and date formats are used. The ECB also provides links to further documentation. |
| R1 | ~ | There is some documentation, but a more detailed explanation of all columns would be helpful. |
| R1.1 | ~ | The reuse conditions are available, but the licence information is not directly included in the CSV metadata. |
| R1.2 | ✓ | The ECB and Eurostat are named as data providers, so the origin of the data is traceable. |
| R1.3 | ✓ | The dataset uses the SDMX standard, which is commonly used for statistical data. |

### Overall assessment

Overall, the dataset fulfils most of the FAIR principles. It is easy to find, download and process. Some information about the data and its reuse conditions could be explained more clearly.

The dataset is publicly available and can be reused under the ECB's conditions. However, this does not automatically mean that it is fully open according to the Open Definition.

### Three things we would improve for our own dataset in Milestone 2

1. **Better documentation:** We would describe all columns, including their meaning, data type and units.
2. **Clear licence:** We would use a clearly stated open licence, for example CC BY 4.0.
3. **More transparency:** We would explain where the data come from, how they were collected and when they were last updated.

This would make our dataset easier to understand, find and reuse.
