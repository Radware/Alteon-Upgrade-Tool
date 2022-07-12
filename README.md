# Multi-Alteon VA Upgrade Tool

Large scale upgrade tool for Alteon VA instances.

## Installation

Download the release version of this project and upload to vDirect.

## Important Information
    -   The image upload is done via SCP and may take some time,
     it is recommended to use the dedicated function 'Upload Image Alteon' to upload the images beforehand.
    - Uploading image must include upgrade password, if it is not needed enter 'None'.   

## Supported Devices

	- Alteon VA

## Prerequisite & Limitations

1. Supported in a wizard mode via UI, API is available upon all inputs.
2. Upgrade is running sequentially, upon failure of single device it will halt next in line devices. 

## General Information

1. The script take a snippet of the Alteon state before the upgrade to be compared afterwards.
2. Compare function is available even after upgrade function. 

## How to install

1. Upload the zip file as is to vDirect workflow template (Inventory->workflow template).
2. create a workflow instance from the workflow template.
3. From this point forward you can re-use the workflow instance for each sync operation.
4. Under the workflow instance (operations->workflows) you should have the following options;
    -  Upgrade Alteon
    -  Upload Image Alteon
    -  Clear Adc Health State
    -  Verify Servers Health

## How to Use 
1. Upgrade Alteon - 
    * Screen #1, shows all available Alteons
    * Screen #2, select ADC
    * Screen #3, leave blank to complete ADC selection
    * Screen #4, Provide destination image name as well SCP details for configuration backup.
2. Upload Image Alteon -
    * Screen #1, shows all available Alteons
    * Screen #2, select ADC and provide upgrade password
    * Screen #3, leave blank to complete ADC selection
    * Screen #4, Provide image location and SCP server credentials
3. Clear Adc Health State -
    * Clears vDirect DB for previous upgrade Alteon state snippet.
4. Verify Servers Health (It is recommended to run it after some time, to allow server health check to pass) -
    * Provides HTML table if anything changed after upgrade.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## CopyRights
Copyright 2022 Radware – All Rights Reserved

## License
[Apache2.0](https://choosealicense.com/licenses/apache-2.0/)

## Tool Snapshot
![](https://i.imgur.com/gCW3gzx.png)

## Disclaimer
There is no warranty, expressed or implied, associated with this product.
Use at your own risk.
