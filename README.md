#### Notice: Veracode is deprecating username and password authentication for Veracode APIs. If this script is not updated to work with Veracode API ID and Key it will stop working once basic auth support is fully removed. PRs welcome.

#### Warning: *This script won't work out of the box. It will require settings or some customization.*

### [shell/veracode.sh](shell/veracode.sh) directory [version]
Arguments:
* directory: **Required**. Directory path containing the files you wish to submit in your scan (not recursive)
* version: Optional. Name of the build version. Will be seen in reports. Default: `date "+%Y-%m-%d %T"`

This script will do the following:

1. Check if a build was left in an incomplete state, if so delete it
2. Create a new build
3. Upload files
4. Initiate pre-scan of files
5. Poll for pre-scan completion
6. Initate scan (will attempt to scan as many of the files as possible)
7. Poll for scan completion
8. Download the reports (detailed PDF, detailed XML, and summary PDF)
9. Email the reports

Dependancies:
* curl
* mailx
