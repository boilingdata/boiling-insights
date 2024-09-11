# Boiling Insights

## INSTALL

Download [Boiling Insights installation file for Mac OSX (arm64)](BoilingInsights-0.7.4-arm64.dmg).

```shell
xattr -d com.apple.quarantine /Applications/Boiling\ Insights.app
```

- **NOTE:** Please note that you may need to remove the Apple Quarantine flag from the app file for now. We are working on notarizing Boiling Insights with Apple to remove this restriction.
- **NOTE:** Bare with us, we're adding support for more archs.

## Run Boiling Insights with AWS Lambda Logs

1. Install [Data Taps](https://github.com/boilingdata/data-taps-template) to get ingestion URL, and then
2. Add [Boiling AWS Lambda Extension](https://github.com/dforsber/data-taps-lambda-extension) to your Lambda functions and
3. Get Boiling Data authorzation token with [`bdcli`](https://github.com/boilingdata/boilingdata-bdcli) and set it into the Lambda Function environment variables (see Data Taps instructions)

## Data Profiles (WIP)

Data Profiles are configurations against known raw data sets.

Boiling Insights currently supports "AWS Lambda Logs" [`aws-lambda-json-logs`](data-profiles/aws-lambda-json-logs/) Data Profile. This data profile includes:

1. Raw data set compaction SQL
2. List of aggregation table SQL derived from the compacted data set
3. A set of Apache Echarts configurations with corresponding SQL clauses for ready made charts
