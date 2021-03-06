# Thinkst Canary AddOn For Splunk

## Canary About
Most companies find out way too late that they have been breached. Even with millions of dollars invested in security, over-worked admins and ignored alerts do little to help.

But what if there were a simpler, more reliable signal than malware signatures? Wouldn't you want to know if someone was opening 'passwords.xls' on \\NetworkTeam_FS1, or brute-forcing an SSH server on your DataBase segment?

Thinkst Canary can be deployed in under 3 minutes (even on complex networks) and is a clear, high quality marker of compromise. Know. When it Matters.

## Overview
This Add-On allows the analyst to collect data from the Canary Tools API.  In addition, Adaptive response actions have been provisioned to allow you to automate responses to alerts

## Thinkst Canary AddOn For Splunk
This Add-On requires access to the Canary Tools API and for the API to be enabled within your Canary Console and the Splunk Common Information Model App located [here](https://splunkbase.splunk.com/app/1621/).  In addition a heavy forwarder will need to be setup as this will act as the server that collects data for indexing.

## Features
- Collect data related to incidents
- Collect data related to devices
- Collect data related to tokens
- Adaptive Response Action to acknowledge incidents
- Adaptive Response Action to delete incidents
- CIM Mapping to Intrusion Detection to enable integration with Splunk Enterprise Security

## Setup
### Canary Tools Setup
1. Visit your Canary Console by going to https://yourconsole.canary.tools/settings
2. Scroll down to API and click on.
3. Enter your password at the top of the page twice
4. Click Save
5. Take note of the generated API key.  You will need this.

### Splunk Installation

1. Install from [Splunkbase](https://splunkbase.splunk.com/app/3980/) (recommended), or git clone this repo ('git clone https://github.com/thinkst/canary_splunk_addon')
2. Install the add-on to the indexer, heavy forwarder and search head in your Splunk environment
3. On the Search Head open a browser to to http://yoursplunkserver:8000/en-GB/app/TA-canary/configuration
4. Enable a proxy if it is required
5. Click Add-on Settings and enter the API Key from Step 5 above.
6. Enter your Canary Domain, if your full domain is https://yourconsole.canary.tools/ then use 'yourconsole'.
7. Click Save
8. Repeat steps 4-7 on the heavy forwarder.
7. If you have proxy rules  allow https://*.canary.tools/ from your Search Head and Heavy Forwarder


## Release Notes
- 1.1.3 Early release with API functionality.
- 1.1.4 Fixed cursor-based fetching for large result sets.
- 1.1.5 Move API token into HTTP header.
- 1.1.6 Finished API migration
- 1.1.7 Fix duplicate values in tabulated view
- 1.1.8 Handle special chars in passwords
- 1.1.9 Additional checks on returned URLs
- 1.1.10 Fix typo
- 1.1.11 Rebuild broken package
- 1.1.12 Include python3 support for Splunk 8
- 1.1.13 Rebuild for explicit python3 support
- 1.1.14 Fix bug in closing incidents
- 1.1.15 Fix issues for being added to Splunk Cloud
- 1.1.16 Fix api_key encryption

## Credits
Written by Mickey Perre, maintained by Thinkst. Kindly file issues with the app here in Github.
