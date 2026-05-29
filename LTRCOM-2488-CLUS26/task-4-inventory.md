# Task 4: Inventory

When configuring UCS, a domain and chassis policy similar to what was created earlier would be applied, and the systems administrator would start seeing the inventory of the Fabric Interconnects, Chassis and Servers populate in Intersight as they are discovered. We will now review the inventory of devices that have been discovered in Intersight.

First, navigate to **Chassis** and select a chassis from the list:

<figure>
<img src="assets/media/image104.png" style="width:4.5429in;height:1.77595in" alt="A screenshot of a computer Description automatically generated" />
</figure>

The chassis details are now displayed for the chassis you selected in the previous step.

<figure>
<img src="assets/media/image105.png" style="width:3.76453in;height:3.39883in" alt="A screenshot of a computer Description automatically generated" />
</figure>

In the upper right section of the Properties column, select **Rear** to change the view and see the rear components installed in the chassis:

<figure>
<img src="assets/media/image106.png" style="width:3.27478in;height:2.56465in" alt="A close-up of a computer Description automatically generated" />
</figure>

Now click on the **Inventory** tab:

<figure>
<img src="assets/media/image107.png" style="width:1.17823in;height:1.97624in" alt="A screen shot of a black screen Description automatically generated" />
</figure>

Select **Intelligent Fabric Module 1** and review the information under the **General**, **Backplane Ports**, **Fabric Ports**, **Fan Modules** and **Graphic View:**

<figure>
<img src="assets/media/image108.png" style="width:3.9279in;height:2.59474in" alt="A screenshot of a computer Description automatically generated" />
</figure>

There are no X-Fabric Modules installed in the chassis, this can be verified by selecting **X-Fabric Modules** and looking for model **UCSX-9508-RBLK** signifying a blank module is installed in each slot.

<figure>
<img src="assets/media/image109.png" style="width:4.75822in;height:2.20238in" alt="A screenshot of a computer Description automatically generated" />
</figure>

The **Thermal** information provides information such as how the Fan Control Mode is configured and the operational state of the Fan Modules:

<figure>
<img src="assets/media/image110.png" style="width:1.28532in;height:1.94388in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Select **Power** to verify the chassis power configuration and how many PSUs are installed.

<figure>
<img src="assets/media/image111.png" style="width:3.70711in;height:2.83961in" alt="A screenshot of a computer AI-generated content may be incorrect." />
</figure>

Now click **Servers** to display a list of all servers populated in the chassis:

<figure>
<img src="assets/media/image112.png" style="width:4.32476in;height:1.32307in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Before we proceed to server inventory, select **Servers** and click on your assigned server.

In this example we are going to look at SRV-17 or RTP91-0FI6454-03-1-1:

<figure>
<img src="assets/media/image113.png" style="width:4.08522in;height:1.64411in" alt="A screenshot of a computer Description automatically generated" />
</figure>

At the **General** tab, you will find the server’s serial number, amount of CPUs, Cores, Memory, Adapters, Firmware version, Alarms and much more:

<figure>
<img src="assets/media/image114.png" style="width:3.40601in;height:2.428in" alt="A screenshot of a computer Description automatically generated" />
</figure>

In the upper right section of the Properties column, select **Top** to change the view and see the internal components of the server:

<img src="assets/media/image115.png" style="width:3.45711in;height:2.03563in" alt="A computer chip with many green slots Description automatically generated with medium confidence" />

Select the **Inventory** tab and then select **Expand All**.

Walk through the various components and review the hardware installed. Under **Storage Controllers**, verify if the server has a **M.2 Controller.** This will be needed for another task. Verify if the server also has NVMe Drives (**Controller NVME-Direct-U.2 Drives**). If your server has NVMe U.2 drives, document the drive names (i.e. **FRONT-NVME-1** or **FRONT-NVME-2**):

<figure>
<img src="assets/media/image116.png" style="width:0.99003in;height:2.86549in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Click the **UCS Server Profile** taband verify that there is no Server Profile assigned:

<figure>
<img src="assets/media/image117.png" style="width:5.626in;height:0.98053in" alt="A screen shot of a computer Description automatically generated" />
</figure>

Click the **HCL** tab and verify the information displayed in the HCL tab (your HCL may look different than what is displayed below:

<figure>
<img src="assets/media/image118.png" style="width:4.59476in;height:2.09933in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Now click the Topology tab to show the connections between the servers, IFMs and Fabric Interconnects:

<figure>
<img src="assets/media/image119.png" style="width:4.02134in;height:2.0792in" alt="A computer screen shot of a server AI-generated content may be incorrect." />
</figure>

Metrics tab information will be reviewed later as there is a task which walks throught the different Metrics in Intersight.

If no server profile is assigned to the server, you should not see any connectivity as shown under the Connectivity tab:

<figure>
<img src="assets/media/image120.png" style="width:6.08304in;height:0.99067in" alt="A screenshot of a computer Description automatically generated" />
</figure>
