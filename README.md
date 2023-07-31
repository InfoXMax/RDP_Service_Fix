# Remote Desktop Service Fix

> A registry script to fix Remote Desktop Service startup issues on Windows Server.

## Table of Contents

- [Description](#description)
- [Problem](#problem)
- [Solution](#solution)
- [How to Use](#how-to-use)
- [License](#license)

## Description

If you are encountering issues with starting the Remote Desktop Service (RDP) on your Windows Server, this registry script might provide a solution. The script addresses common problems by modifying the necessary registry entries for the RDP service.

**Warning**: Modifying the registry can have serious consequences if done incorrectly. Make sure you understand the changes being made or create a backup of your registry before applying the fix.

## Problem

The Remote Desktop Service (TermService) is critical for allowing remote desktop connections to the server. However, some users have reported that the service is not found or fails to start, preventing remote access to the server.

## Solution

This repository contains a registry script (`remote_desktop_service_fix.reg`) that can help resolve the issue with the missing or non-starting Remote Desktop Service. The script sets the appropriate registry values to ensure the service's proper functioning.

## How to Use

To apply the fix, follow these steps:

1. Download the `remote_desktop_service_fix.reg` file .
2. Double-click the downloaded `.reg` file to apply the changes to your registry.
3. If prompted, confirm the changes and allow the script to make modifications.

After applying the fix, try restarting your computer and check if the Remote Desktop Service starts correctly. You should be able to establish remote desktop connections to your Windows Server.


## Registry Keys

The script modifies the following registry keys:

- HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\TermService\Parameters
- ServiceDll: %SystemRoot%\System32\termsrv.dll

These keys are crucial for the proper functioning of the Remote Desktop Service.


If you encounter any issues with the fix or have suggestions for improvements, feel free to [open an issue](https://github.com/InfoXMax/RDP_Service_Fix/issues). 


## License

This project is licensed under the [MIT License](LICENSE).
