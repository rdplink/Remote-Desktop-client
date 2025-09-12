## Remote Desktop client for Azure Virtual Desktop

This guide explains how to connect to Azure Virtual Desktop using the Remote Desktop client.

Follow the steps below to install the Remote Desktop client on Windows via the MSI installer. For enterprise deployments, the `msiexec` command can be run from the terminal to perform a silent installation.

1. Download the Remote Desktop client installer version that matches your operating system:

* [Windows 64-bit](https://github.com/encrowd/Remote-Desktop-client/releases/tag/1.508)  *(most common)*
* [Windows 32-bit](*)
* [Windows ARM64](*)

2. Launch the installer by double-clicking the downloaded file.

3. When the welcome screen appears, click **Next**.

4. To accept the license agreement, check **I accept the terms in the License Agreement** and continue by clicking **Next**.

5. On the Installation Scope page, select one of the following options:

* **Install just for you**: Installs Remote Desktop to a user-specific directory. Only your account will have access, and Administrator privileges are not required.

* **Install for all users of this machine**: Installs Remote Desktop for all accounts on the device. This option requires Administrator rights.

6. Click **Install** to begin the installation.

7. Once setup completes, select **Finish**.

8. If **Launch Remote Desktop when setup exits** is checked, the client will start automatically. Otherwise, launch it manually by searching for **Remote Desktop** in the Start menu.

> **Important**
> If both the Remote Desktop client and the Azure Virtual Desktop app from Microsoft Store are installed on the same machine, you may see a prompt like **A version of this application called Azure Virtual Desktop was installed from the Microsoft Store**. Although both are supported, switching between them for the same resources can cause confusion. For consistency, use only one version.

Before connecting to remote resources on Windows, ensure you have:

* A working internet connection

* A device running a supported Windows edition:

  * Windows 11
  * Windows 10
  * Windows Server 2022
  * Windows Server 2019
  * Windows Server 2016

* .NET Framework 4.6.2 or newer. Certain Windows 10 and Windows Server 2016 builds may require manual installation. Visit the official .NET Framework download page for the latest version.

## Subscribe to a workspace

A workspace contains all desktops and applications provided by your administrator. To access these resources with the Remote Desktop client, subscribe to a workspace as follows:

1. Open the **Remote Desktop** app on your device.

2. If this is your first subscription, on the **Let's get started** screen, choose either **Subscribe** or **Subscribe with URL**.

* Selecting **Subscribe** requires signing in with your credentials (e.g., `user@contoso.com`). After a few moments, the desktops and applications assigned to you will appear.

If you see **No workspace is associated with this email address**, email-based discovery may not be set up or you may be in a specialized Azure environment, such as Azure Government. In that case, use **Subscribe with URL**.

* Choosing **Subscribe with URL** requires entering the given URL in the **Email or Workspace URL** field. After a few seconds, you should see **We found Workspaces at the following URLs**.

3. Click **Next**.

4. Enter your login credentials when prompted. After a brief delay, the workspace will load with the desktops and apps assigned by your administrator.

Once subscribed, the workspace refreshes periodically and each time you open the client. Administrators may add, modify, or remove resources as needed.

## Connect to your desktops and applications

To launch your desktops and apps:

1. Open the **Remote Desktop** client on your device.

2. Double-click any icon to start a session with Azure Virtual Desktop. Depending on your organization’s setup, you might need to re-enter your password.
