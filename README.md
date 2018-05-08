# MarkDownStyling
This is a rough repo to test out various styling options available with Markdown

# Retailer Shopper Profile
The vision was to get a dictionary of all behavioral features, given a liveramp_id. This folder contains codes used to automate creation of the base avro file that would enable the same.

### List of Contents

| Name of Folder / File   |  Utility / Contents     |
| :-----------------------|:----------------------- |
| VariableLogics          |This folder contains individual codefiles for each attribute|
| ContributionsByDeveloper|This contains Developer wise folders. Each of those has two files. One with all the functions / variable logics and other with function calls according to the integration standards                       |
| SupportFunctions        |This folder contains the code architecture used for this project. Verification and other support functions can also be found here|
| SampleGcloudCode        |This contains a sample code that could be pasted into the gcloud console to execute the script|

### Schema of the Base Avro File

| Column Name             |  Variable Type          | Description             |
| :-----------------------|:----------------------- |-------------------------|
| liveramp_id             |StringType               |This is a unique identifier for each shopper|
| category_code           |StringType               |This has the combination of categories separated by an underscore. O represents overall level |
| as_of_date              |StringType               |This has the date for which these attributes has been created. A year of data up till this date is considered for creation of the corresponding feature|
| retailer_id             |StringType               |The retailer_id corresponding to the observation|
| partner_id              |StringType               |The partner_id corresponding to the observation|
| key_value               |MapType(key : StringType, value : StringType)|This is a python dictionary containing values for each attribute / key|

