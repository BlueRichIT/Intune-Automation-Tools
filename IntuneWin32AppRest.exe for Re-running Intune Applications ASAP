Overview

When a Win32 application deployment fails in Microsoft Intune, the device typically does not retry the installation immediately. This is due to Intune’s Global Re-evaluation Schedule (GRS), which can delay the next installation attempt for up to 24 hours.

IntuneWin32AppRest.exe provides a simple GUI-based solution to force an immediate retry of failed Intune Win32 applications by resetting the local Intune Management Extension (IME) state and triggering a fresh evaluation.

Important: This tool does not uninstall applications. It only resets the local Intune installation state so Intune can immediately re-evaluate and reattempt the deployment.

What Problem Does This Tool Solve?
A Win32 application fails to install.
Intune marks the application deployment as failed.
GRS prevents another installation attempt for approximately 24 hours.
Waiting for the next retry delays testing, troubleshooting, and urgent deployments.

IntuneWin32AppRest.exe removes the local retry delay state, allowing Intune to attempt the installation again immediately.

What Does IntuneWin32AppRest.exe Do?

The tool performs the following actions:

Search
Locates registry entries associated with the selected Win32 application using its AppId (unique application identifier).

Match
Extracts the related GRS Hash from Intune Management Extension log files to accurately identify the retry-related registry entries.

Reset
Removes only the Intune Management Extension registry state associated with the specified AppId and GRS Hash.

Re-evaluate
Triggers the Intune Management Extension to immediately re-evaluate the application deployment and initiate a retry.

What Does the Tool NOT Do?
Does not uninstall the application.
Does not remove application files.
Does not execute uninstall commands.
Does not modify application content.

The installed application remains untouched.

When Should You Use This Tool?

Use IntuneWin32AppRest.exe when:

A Win32 application installation has failed and requires an immediate retry.
Troubleshooting Win32 application deployments.
Testing installation logic, detection rules, requirements, or dependencies.
Avoiding the standard Intune GRS waiting period.
Accelerating validation during packaging and deployment testing.

How to Find the AppId in Intune
Navigate to Intune Admin Center → Apps → All Apps.
Open the target Win32 application.
Review the browser URL.
Copy the value following /appId/.

Example:
https://intune.microsoft.com/#view/Microsoft_Intune_Apps/SettingsMenu/~/0/appId/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx

The GUID shown after /appId/ is the AppId required by the tool.

How to Use IntuneWin32AppRest.exe
Requirements
Run as Administrator or SYSTEM.
Intune Management Extension must be installed on the device.
Supported on Intune-managed Windows devices.
Steps
Launch IntuneWin32AppRest.exe.
Enter or select the required AppId.
Start the reset process.
The tool will identify and remove the relevant IME deployment state.
Intune Management Extension will immediately re-evaluate the application deployment.
Monitor the Intune Management Extension logs and Company Portal for deployment status.

Example Scenario

A Win32 application fails because of a temporary network interruption. Intune marks the deployment as failed and schedules the next retry for the following day.

Instead of waiting:

Find the application's AppId in Intune.
Open IntuneWin32AppRest.exe.
Enter the AppId and initiate the reset process.
The tool clears the relevant IME state.
Intune re-evaluates the deployment and retries the installation within minutes.

Summary

Problem: Intune delays Win32 application retries because of the Global Re-evaluation Schedule (GRS).

Solution: Use IntuneWin32AppRest.exe to reset the local Intune Management Extension state and force immediate re-evaluation.

Key Components:

AppId
GRS Hash
Intune Management Extension (IME)

Result: Faster troubleshooting and immediate retry of failed Win32 application deployments.

Disclaimer

IntuneWin32AppRest.exe is provided as-is without any warranty. Use it at your own risk and thoroughly test in a non-production environment before deployment in production.
