# GNS3 Setup Guide

## Part 1: Installation

1. Visit the download page at <https://www.gns3.com/software/download>. You'll need to sign up first.

   ![GNS3 download page](images/01-download-page.png)

2. The link above downloads the GNS3 all-in-one `.exe` file. Once it finishes, go to where it was downloaded and double-click to install.

   ![Downloaded installer](images/02-installer-file.png)

   If it prompts for any options, leave the defaults and continue. The installer will install both GNS3 and TraceNG.

3. After installation, double-click the GNS3 icon on the desktop (it looks like the icon of the installer above) and start the application. If it is the first time installing GNS3, you'll get the following screen.

   ![Setup Wizard: Server](images/03-wizard-server.png)

   Choose the **second option** (_Run appliances on my local computer_) for now, then click **Next**.

   ![Setup Wizard: Local server configuration](images/04-wizard-local-server.png)

   Leave the defaults and click **Next**.

   ![Setup Wizard: Local server status](images/05-wizard-server-status.png)

   Once it shows successful, click **Next**. It will show a summary. Click **Next** again and you'll get a blank canvas.

   ![Blank GNS3 canvas](images/06-blank-canvas.png)

   Make sure the server is running properly (the **Servers Summary** entry should show green). If it does, the installation is successful.

---

## Part 2: Installing Appliances

In GNS3, appliances are preconfigured virtual machine templates (switches, routers, firewalls) that make it easier to add and run network devices inside GNS3.

### Step 1: Download an appliance

Go to <https://gns3.com/marketplace/appliances>.

### Step 2: Choose an appliance

We'll choose the **Cisco 7200** and download it.

![GNS3 marketplace appliance list](images/07-appliance-marketplace.png)

### Step 3: Import the appliance

Go back to GNS3 and on the toolbar click **File → Import appliance**.

![File menu: Import appliance](images/08-file-import-appliance.png)

It will open File Explorer. Browse to where the appliance was downloaded, most likely the Downloads folder, and choose it. (The appliance has the extension `.gns3a`.)

![Downloaded .gns3a file](images/09-appliance-file-explorer.png)

It will bring up the options below. Choose the option to install the appliance on your **local computer**.

![Install appliance: server type](images/10-appliance-server-type.png)

If there are no installation instructions, as shown below, click **Next**.

![Installation instructions: none available](images/11-appliance-no-instructions.png)

On the next step it will prompt you for the GNS3 image to use.

![Required files: all missing](images/12-required-files-missing.png)

If all options are shown in red as "Missing" like above, we'll need to manually download the images for the router. Take note of the name of the `.image` file at the top. In this case it is:

**`c7200-adventerprisek9-mz.153-3.XB12.image`**

### Step 4: Downloading images

Go to <https://github.com/hegdepavankumar/Cisco-Images-for-GNS3-and-EVE-NG>.

The GitHub page has a wide range of images. Scroll through the page and look for the section that says **Cisco Images FOR GNS3**. Then look for the image with the same name as the one noted above (or something very similar) and download it.

![Cisco Images for GNS3 list](images/13-cisco-images-github.png)

Make sure the downloaded image is saved in your Downloads folder.

### Step 5: Installing the image

Go back to the GNS3 application and click **Refresh**.

![Required files dialog with Refresh button](images/14-required-files-refresh.png)

The status beside the image you downloaded will turn green and say **Ready to install**. If not, make sure it is in your Downloads folder.

![Version showing Ready to install](images/15-ready-to-install.png)

Click on that line with green, then click **Next**. If a confirmation message pops up, click **OK**.

![Ready-to-install version selected](images/16-ready-to-install-selected.png)

If successful it will show something like below. Click **Finish**.

![Appliance usage screen](images/17-appliance-usage.png)

---

## Part 3: Configuring the Router

By default the c7200 comes with few interfaces. To add more, on the toolbar click **Edit → Preferences**.

![Edit menu: Preferences](images/18-preferences-menu.png)

In the Preferences window, look for **IOS routers** under **Dynamips**, click on **Cisco 7200**, then click **Edit**.

![IOS router templates](images/19-ios-router-templates.png)

In the new window that pops up, click the **Slots** tab.

![Slots tab](images/20-slots-tab.png)

Then click **slot 1** and choose at least **PA-2FE-TX** to get two more Fast Ethernet ports.

![Slot adapter dropdown](images/21-slot-dropdown.png)

If more ports are needed, you can also add in slot 2: **PA-GE** for Gigabit Ethernet or **PA-4T+** for serial interfaces. Then at the bottom click **OK**.

![Slots dialog OK button](images/22-slots-ok.png)

Then click **Apply** and then **OK** again.

![Preferences: Apply and OK](images/23-apply-preferences.png)

---

## Part 4: Creating a Project

In order to start using the new router you need to create a new project.

### Step 1

On the toolbar click **File → New blank project**.

![File menu: New blank project](images/24-new-blank-project.png)

### Step 2

Give the project a name and then click **OK**.

![New project dialog](images/25-project-name-dialog.png)

### Step 3: Adding devices to the project

To add devices to the project, choose templates from the left sidebar, which looks like this:

![Device sidebar: Routers, Switches, End devices, Security devices, All devices, Cable](images/26-device-sidebar.png)

From top to bottom the sidebar categories are: **Routers**, **Switches**, **End devices**, **Security devices**, **All devices**, and **Cable**.

Choose the option for routers and then drag and drop the Cisco 7200 that we installed into the workspace.

![Cisco 7200 router placed on the canvas](images/27-router-on-canvas.png)

To turn on the router, click the green button at the top.

![Start button in the toolbar](images/28-start-button.png)

Then, to configure the router, right-click on the router and click **Console**.

![Right-click menu: Console](images/29-console-menu.png)

It will open up a terminal emulator (SolarPuTTY by default). Wait for it to load the IOS. After it loads, you'll see the normal router console prompt inside the terminal emulator, just like in Packet Tracer:

![Router console prompt](images/30-console-output.png)

_The end._
