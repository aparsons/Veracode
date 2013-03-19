### shell/veracode.sh [Directory] [Version]
Arguments:
* Directory: Required. Directory path containing the files you wish to submit in your scan (not recursive)
* Version: Optional. Name of the build version. Will be seen in reports. Default: `date "+%Y-%m-%d %T"`

This script will 
# Check if a build was left in an incomplete state, if so delete it
# Create a new build
# Upload files
# Initiate pre-scan of files
# Poll for pre-scan completion
# Initate scan (will attempt to scan as many of the files as possible)
# Poll for scan completion
# Download the reports (detailed PDF, detailed XML, and summary PDF)
# Email the reports

Dependancies
* curl
* mailx
