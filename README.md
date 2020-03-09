# Sql Writer Data Validation

The purpose of this tool is to verify that the data generated by Looker's new SQL writer is the same as the old SQL writer.

Requirements:
1. macOS with Ruby (min version 2.4.4) installed. We recommend installing Ruby with a Package Manager such as Homebrew. Installation instructions for Ruby can be found under the Homebrew section at: https://www.ruby-lang.org/en/documentation/installation/

# Script Execution Steps

**Make sure to set the following variables in the spec/config.yml file.**

1. **DASHBOARD_IDS** - This is the list of Dashboard IDs you'd like to run this tool against. You can query the top used Dashboards in the Admin--> Usage section of Looker. We'd recommend inputting atleast top 100 used Dashboards if posssible.
2. **CLIENT_ID** and **CLIENT_SECRET**, these are the API3 keys for a user found in User Settings  
(Instructions for generating API3 Keys: https://docs.looker.com/admin-options/settings/users#api3_keys)
3. **API_BASEURL** - This is the address of your Looker instance (ex: https://your_instance.looker.com)
4. Finally you can run the sql_writer_tests.sh script located in the looker-data-validation directory by executing the following command in your macOS Terminal: **sh sql_writer_tests.sh**

# General notes

1. The data fetched from the dashboards is stored in looker-data-validation/spec/results/data (should be deleted once no longer needed)
2. The SQL fetched from the dashboards is stored in looker-data-validation/spec/results/sql (should be deleted once no longer needed)
3. The debug log (data_validation.log) is stored in looker-data-validation/spec/results
