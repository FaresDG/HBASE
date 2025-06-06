#  HBase Assignment – Los Angeles Crime Data

## Objective

This project aims to practice loading and querying a large dataset using **Apache HBase**, interacting via the **HBase Shell** and **Python (HappyBase)**, all within a **Docker** environment. The dataset used is a sample of crime reports in Los Angeles.

You will:
- Explore the dataset with Python
- Design a schema for HBase
- Insert and query the data
- Analyze the results



## Technologies Used

- [Docker](https://www.docker.com/)
- [Apache HBase](https://hbase.apache.org/)
- Python (with `pandas`, `happybase`)
- GitHub



## 🔧 Setup Instructions

### 1. Clone the Repository

```bash
git clone https://github.com/FaresDG/HBASE.git
cd HBASE

2. Launch Docker Environment
Ensure Docker & Docker Compose are installed

Create a docker-compose.yml file including HBase and optional HBase UI

Start services:

bash
Copier
Modifier
docker-compose up -d
Access HBase shell:

bash
Copier
Modifier
docker exec -it hbase /bin/bash
hbase shell


📊 Part 1: Exploratory Data Analysis (EDA)
Using Python and pandas:

Load the CSV file sample_crimes_data.csv

Display:

Number of rows and columns

Missing values

Crime categories

Area analysis

Time distribution (month, year)

Visualize insights with charts

This analysis guides schema design for HBase.

🧱 Part 2: HBase Data Modeling
Create a namespace:

hbase
Copier
Modifier
create_namespace 'practice'
Design a table: practice:crimes with column families:

location

crime_info

Use a composite row key:
Format: salt_drno_date (e.g., 12_190326475_20200101)

Document design choices in the report.

🧪 Part 3: Data Insertion with Python
Clean and rename columns (snake_case)

Use happybase to connect to HBase

Map columns to families using a catalog

Convert datetime to string format

Skip cells with missing values (NaN)

Insert at least 500,000 rows





## Retrieve & Analyze from Python
Using Python:

Retrieve SHOPLIFTING & VANDALISM crimes

Crimes in Hollywood

Victim data for INTIMATE PARTNER - SIMPLE ASSAULT

