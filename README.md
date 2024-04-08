# a) Read data from different formats
# CSV file
data_csv <- read.csv("file.csv")

# Excel file
library(readxl)
data_excel <- read_excel("file.xlsx")

# b) Indexing and selecting data, sort data
# Indexing
selected_data <- data_csv[1:10, c("column1", "column2")]

# Sorting
sorted_data <- data_csv[order(data_csv$column1), ]

# c) Describe attributes of data, checking data types of each column
summary(data_csv)
str(data_csv)

# d) Counting unique values of data, format of each column, converting variable data type
# Count unique values
unique_values <- unique(data_csv$column1)

# Convert data type
data_csv$column1 <- as.factor(data_csv$column1)

# e) Identifying missing values and fill in the missing values
# Check missing values
missing_values <- is.na(data_csv)

# Fill missing values
data_csv[is.na(data_csv)] <- 0
import pandas as pd

# a) Read data from different formats
# CSV file
data_csv = pd.read_csv("file.csv")

# Excel file
data_excel = pd.read_excel("file.xlsx")

# b) Indexing and selecting data, sort data
# Indexing
selected_data = data_csv.loc[0:9, ["column1", "column2"]]

# Sorting
sorted_data = data_csv.sort_values(by="column1")

# c) Describe attributes of data, checking data types of each column
data_csv.info()
data_csv.describe()

# d) Counting unique values of data, format of each column, converting variable data type
# Count unique values
unique_values = data_csv["column1"].unique()

# Convert data type
data_csv["column1"] = data_csv["column1"].astype("category")

# e) Identifying missing values and fill in the missing values
# Check missing values
missing_values = data_csv.isnull()

# Fill missing values
data_csv.fillna(0, inplace=True)
