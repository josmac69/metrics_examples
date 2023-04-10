# Data Quality Metrics

ChatGPT:

Data quality metrics are crucial for assessing the accuracy, completeness, and overall usability of a dataset. Here is a list of common data quality metrics, along with descriptions, measurement methods, and examples when applicable:

Accuracy:
* Meaning: The degree to which data correctly represents the real-world entities or events it describes.
* Measurement: Compare the data values against a trusted source or standard.
* Example: Check if product prices in a database match the actual prices listed on a company's website.

Completeness:
* Meaning: The proportion of essential data elements that are present and populated in the dataset.
* Measurement: Calculate the ratio of non-missing values to the total expected values for each data element.
* Example: Determine the percentage of customers with complete contact information in a CRM system.

Consistency:
* Meaning: The adherence of data values to a defined format, structure, or standard across the dataset.
* Measurement: Identify data elements that violate consistency rules or have conflicting information.
* Example: Ensure that all dates in a dataset follow the same format (e.g., YYYY-MM-DD).

Uniqueness:
* Meaning: The absence of duplicate data entries within the dataset.
* Measurement: Identify and count duplicate records or data elements.
* Example: Check if there are multiple customer records with the same email address in a database.

Timeliness:
* Meaning: The degree to which data is up-to-date and available when needed.
* Measurement: Compare the age of the data to a defined threshold or acceptable time range.
* Example: Verify that financial data is updated at least once per quarter.

Validity:
* Meaning: The extent to which data values conform to specified business rules or constraints.
* Measurement: Check data values against predefined validation rules (e.g., range checks, format checks).
* Example: Ensure that all phone numbers in a dataset follow a specific pattern, such as (XXX) XXX-XXXX.

Integrity:
* Meaning: The preservation of relationships, dependencies, and linkages between data elements.
* Measurement: Identify violations of referential integrity rules, such as orphaned or missing foreign key values.
* Example: Check if all order records in a database have a valid customer ID associated with them.

Granularity:
* Meaning: The level of detail or resolution of the data, ensuring it's suitable for its intended purpose.
* Measurement: Assess if the data's granularity aligns with the required level of detail for analysis or decision-making.
* Example: Determine if sales data is available at the daily, weekly, or monthly level, depending on the reporting needs.

Precision:
* Meaning: The level of exactness or detail captured in the data, often in terms of the number of decimal places or significant digits.
* Measurement: Compare the data's precision to a defined threshold or acceptable range.
* Example: Verify that GPS coordinates in a dataset are precise to at least four decimal places.

Reliability:
* Meaning: The degree to which data remains consistent and accurate over time.
* Measurement: Monitor data quality metrics over time and identify trends or fluctuations in data quality.
* Example: Track the percentage of accurate product prices in a database over multiple months to gauge reliability.

By measuring these data quality metrics, organizations can identify areas for improvement, enhance data quality, and ensure that data-driven decisions are based on reliable information.

***

ChatSonic:

Here's a list of data quality metrics along with their definitions and how to measure them:

1. Completeness: The percentage of missing values in a dataset. It can be measured by dividing the number of non-null values by the total number of records in the dataset. For example, if a dataset has 100 records and 10 of them have missing values, the completeness metric would be 90%.

2. Accuracy: The degree to which data reflects the true value or state of reality. It can be measured by comparing the data to a trusted source or by manual inspection. For example, if a dataset contains the weight of a product and the actual weight is 5 pounds, but the dataset records it as 4.5 pounds, then the accuracy metric would be 90%.

3. Consistency: The degree to which data is uniform and free from contradictions. It can be measured by comparing data across different sources or by using business rules. For example, if a dataset contains the age of customers and some records show negative numbers or numbers over 100, then the consistency metric would be low.

4. Validity: The degree to which data conforms to predefined rules or constraints. It can be measured by using business rules or data validation checks. For example, if a dataset contains email addresses and some records have invalid formats, then the validity metric would be low.

5. Timeliness: The degree to which data is current and up-to-date. It can be measured by comparing data to the expected update frequency or by using timestamps. For example, if a dataset is expected to be updated daily but hasn't been updated in a week, then the timeliness metric would be low.

6. Uniqueness: The degree to which data is unique and not duplicated. It can be measured by using data profiling tools or by manual inspection. For example, if a dataset contains customer IDs and some records have duplicate IDs, then the uniqueness metric would be low.

7. Integrity: The degree to which data is consistent and accurate across different systems or datasets. It can be measured by comparing data across different sources or by using data reconciliation tools. For example, if a dataset contains customer information and the same customer record has different data across different systems, then the integrity metric would be low.

These are some of the most common data quality metrics. By measuring these metrics, organizations can identify areas for improvement and take steps to improve data quality.

***

