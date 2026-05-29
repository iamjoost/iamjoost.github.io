# Task 6: Deploying Server Profiles

Now that we have a UCS Server Profile Template, and we have derived a server profile from it, we can assign it to a physical server.

On the left side of your screen, navigate to **Configure** -\> **Profiles** and you will see the status **Not Deployed** next to your server:

<figure>
<img src="assets/media/image190.png" style="width:5.5839in;height:2.43554in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Click the three dots on the right and click on **Deploy:**

<figure>
<img src="assets/media/image191.png" style="width:1.74297in;height:1.06424in" alt="A screenshot of a computer program Description automatically generated" />
</figure>

A warning message will appear. Select **Reboot Immediately to Activate** and then click **Deploy:**

<figure>
<img src="assets/media/image192.png" style="width:4.54157in;height:2.22134in" alt="A screenshot of a computer program Description automatically generated" />
</figure>

A green message will appear for a couple of seconds in the browser.

<figure>
<img src="assets/media/image193.png" style="width:3.24959in;height:0.95511in" alt="A screenshot of a video chat Description automatically generated" />
</figure>

Click on the checkmark icon at the top of the browser to see the status:

<figure>
<img src="assets/media/image194.png" style="width:3.44293in;height:0.71559in" alt="A screen shot of a computer Description automatically generated" />
</figure>

If you click **Deploy Server Profile**, you see a bit more information:

<figure>
<img src="assets/media/image195.png" style="width:5.08781in;height:2.01726in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Go back to the server profiles and you see the validation state.

<figure>
<img src="assets/media/image196.png" style="width:3.86939in;height:0.8201in" alt="A screenshot of a phone Description automatically generated" />
</figure>

If you see a checkmark at the top and you only see “Validating”, just click templates and go back to Profiles:

<figure>
<img src="assets/media/image197.png" style="width:1.58347in;height:0.50004in" alt="A white circle with a check mark in it Description automatically generated" />
</figure>

After a while you will see the status Activating:

<figure>
<img src="assets/media/image198.png" style="width:3.62936in;height:0.77941in" alt="A screen shot of a video Description automatically generated" />
</figure>

Have a nice break and ask questions to the proctors. They are here for you. After about 15-20 minutes, the server profile is deployed and you will see OK.

<figure>
<img src="assets/media/image199.png" style="width:3.00919in;height:0.69039in" alt="A black screen with blue text Description automatically generated" />
</figure>

If you see a Failed status, click on it and investigate what the problem is.

The proctors can help you.

<figure>
<img src="assets/media/image200.png" style="width:3.71527in;height:0.75309in" alt="A screenshot of a profile Description automatically generated" />
</figure>

### Task 5: Install Operation System

Start with this task only when your Server Profile is deployed on your server and has the status OK.

There are different ways to install an operating system on a server:

- KVM console

- Mount a local ISO and boot to it

- software repository

In the next steps, we will install the OS on the server via the “Install Operating System” option.

There are several ISOs in the software repository. This can be found under **System / Software Repository:**

<figure>
<img src="assets/media/image201.png" style="width:4.64414in;height:1.81122in" alt="A screenshot of a computer Description automatically generated" />
</figure>

## Step 1: Install OS

Navigate to **Operate** -\> **Server, click the three dots found** to the right side of the screen next to your server, and select **Install Operating System**:

<figure>
<img src="assets/media/image202.png" style="width:1.26695in;height:2.375in" alt="A screen shot of a computer Description automatically generated" />
</figure>

Make sure only your server is selected and click **Next**:

<figure>
<img src="assets/media/image203.png" style="width:4.81222in;height:2.42674in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Select the **VMWare80** OS image and click **Next**:

<figure>
<img src="assets/media/image204.png" style="width:3.61706in;height:2.53194in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Do not change the “Select Configuration Source’

Change the IP configuration to **DHCP**, fill in the hostname with your Server ID, use **UCSX@Cisco123** as the password, and click **Next**:

<figure>
<img src="assets/media/image205.png" style="width:4.37292in;height:2.33639in" alt="A screenshot of a computer Description automatically generated" />
</figure>

This method needs SCU to install the OS. For this lab, the SCU image is already uploaded. Select the SCU and click **Next**.

<img src="assets/media/image206.png" style="width:3.2634in;height:2in" alt="A screenshot of a computer Description automatically generated" />

Depening on the server configuration, there are multiple ways to install the OS on a disk. For this lab, configure the installation target to use the M.2 drives and click **Next**:

<figure>
<img src="assets/media/image207.png" style="width:2.95189in;height:1.67708in" alt="A screenshot of a computer program Description automatically generated" />
</figure>

The view you have right now is the summary. Click on **View Details** for a bit more information.

<figure>
<img src="assets/media/image208.png" style="width:5.02756in;height:3.69167in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Click **Install,** then click **Install** again on the warning message:

<figure>
<img src="assets/media/image209.png" style="width:2.98115in;height:1.73181in" alt="A screenshot of a computer error Description automatically generated" />
</figure>

The installation will start.

<figure>
<img src="assets/media/image210.png" style="width:3.38945in;height:0.89468in" alt="A screenshot of a computer Description automatically generated" />
</figure>

To view the progress, you can click the checkmark at the bar or og the the server KVM Console.

Go to the **Server** view and select the three dots to the right of your server. **Select Launch Tunneled vKVM**. This features doesn’t require a VPN connection to the network where the server is located.

<figure>
<img src="assets/media/image211.png" style="width:1.44026in;height:2.54687in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Another web browser tab is opened. It is possible you won’t see anything for a couple of minutes. **The total installation can take between 45 and 60 minutes.** Feel free to proceed with the rest of the lab and come back later for further review.

Below is an example of what you should see in the KVM window once the OS is installed. Note the servername and IP address (should be in the range of 172.20.70.x/24)

<figure>
<img src="assets/media/image212.png" style="width:4.78354in;height:2.18676in" alt="A screenshot of a computer Description automatically generated" />
</figure>

## Step 2: Server Inventory after OS Installation

Now that the server has a profile and the OS is installed, let’s go back to the server and have a closer look at what more information you will see right now.

Click on **Servers** and **select your server.** This will direct you to the general properties of the server:

<figure>
<img src="assets/media/image213.png" style="width:5.401in;height:2.05238in" alt="A computer server with a green and white label Description automatically generated with medium confidence" />
</figure>

Click on **HCL**. The server software compliance should show incomplete. The OS was installed, but the drivers weren’t installed. Click **Get Recommended Drivers:**

<figure>
<img src="assets/media/image214.png" style="width:7.40393in;height:4.30461in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Select OS Vendor: **Red Hat** and the OS Version is **9.3. Intersight will show** the recommended driver versions and will provide a link for downloading the driver ISO. We will not download the ISO for this lab. Click **Close**:

<figure>
<img src="assets/media/image215.png" style="width:3.54603in;height:2.88748in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Click the **Topology** tab. Prior to deploying a server profile, an image of the FIs and IFMs were displayed but now that a Server Profile and OS have been deployed to the server, you see the vNICs connection to the IFM:

<figure>
<img src="assets/media/image216.png" style="width:4.52684in;height:3.33046in" alt="A computer screen shot of a computer Description automatically generated" />
</figure>

Now click the **Connectivity** tab. This should display vETH0 and vETH1 are up and running but vHBA-A and vHBA-B are down:

<figure>
<img src="assets/media/image217.png" style="width:6.52168in;height:1.55437in" alt="A screenshot of a computer Description automatically generated" />
</figure>
