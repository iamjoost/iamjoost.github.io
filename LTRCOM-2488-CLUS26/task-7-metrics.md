# Task 7: Metrics

Cisco Intersight collects metrics for devices that are part of an Intersight Manage Mode (IMM) or UCSM Managed (UMM) domain. Only environmental metrics are collected for UMM devices. The collected metrics are then exposed as widgets on dashboards, and can also be analyzed using custom metrics explorations.

## Step 1: Dashboard Metrics

The main **Dashboards** page will show several Dashboards that can be added or removed to suit the particular account. In this account, these dashboards include various metrics and metric widgets. These metrics include **Power & Energy Metrics, Fabric Interconnects Metrics, and more.**

<figure>
<img src="assets/media/image218.png" style="width:7.70834in;height:4.76042in" />
</figure>

In this lab we will go over **Power and Energy Metrics, Fabric Interconnects Metrics, and Servers Metrics.**

<figure>
<img src="assets/media/image219.png" style="width:7.70834in;height:0.77083in" />
</figure>

Take a look at this page and try to understand which values could be useful for your own environment.
Would you like to know the overall Energy consumption for the account, or for just the Servers?

Select **Power & Energy Metrics**

There are many different types of widgets. You can edit and add relavant widgets to the Dashboard as required.

<figure>
<img src="assets/media/image220.png" style="width:5.10044in;height:1.75849in" alt="A screenshot of a phone Description automatically generated" />
</figure>

You can also modify the information for a given widget. <img src="assets/media/image221.png" style="width:7.90972in;height:1.01528in" alt="A black and white rectangular object Description automatically generated" />

## Step 2: Fabric Interconnect Dashboard Metrics

The Fabric Interconnects have many ports and network metrics can provide details about these ports. For example, you may be interested in checking for any network congestion. <img src="assets/media/image222.png" style="width:7.70834in;height:4.04167in" />

Figure

Clicking on any FI port in the main view will take you to the **Ports and Port Channels** page for the respective Fabric Interconnect:

<img src="assets/media/image223.png" style="width:7.70834in;height:4.01042in" />

Figure 213

Navigate back to the main **Dashboards** page. If you scroll down towards the bottom of the page, you will see several other useful widgets. For example, the widget below shows if there are any errors on any of the server ports.

<figure>
<img src="assets/media/image224.png" style="width:7.90972in;height:2.66042in" alt="A screenshot of a computer Description automatically generated" />
</figure>

## Step 3: Dashboard Server Metrics

The next Dashboard metrics we will cover are the **Servers Metrics**. The current dashboard shows only Temperature metrics, but just like other dashboards, additional widgets can be added as desired. The current widgets show the top 5 servers as they relate to both CPU temperature and ambient (inlet) temperature. This can be an easy way to see if a particular server is having thermal or cooling problems.

<figure>
<img src="assets/media/image225.png" style="width:7.90972in;height:2.68194in" alt="A screen shot of a graph Description automatically generated" />
<figcaption><p>Figure 215</p></figcaption>
</figure>

You can modify the data displayed for the current widgets or add new widgets. To add a new widget, click the Add Widget button on the right hand side.

<figure>
<img src="assets/media/image226.png" style="width:7.70834in;height:0.73958in" />
</figure>

Click the Servers checkbox, and explore the various other widgets related to Servers.

<figure>
<img src="assets/media/image227.png" style="width:3.24573in;height:2.3378in" />
</figure>

## Step 4: Server Metrics

We are now going to explore metrics as they relate to a specific Compute device. Just like you can look at overall metrics for the entire account, there are metrics that can be explored for a single server.

Let’s go back to **Operate / Servers** and select your server.

On the bar, you see Metrics. Click it.

<figure>
<img src="assets/media/image228.png" style="width:5.90885in;height:0.49171in" />
</figure>

Here the Host Power and Temperature are shown.

<figure>
<img src="assets/media/image229.png" style="width:7.17361in;height:3.14027in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Click on the icon next to the mini graphic of Host Power

<figure>
<img src="assets/media/image230.png" style="width:7in;height:0.36in" />
</figure>

An exploded view is now visible.

Change the **Time Interval** setting to last month.

<figure>
<img src="assets/media/image231.png" style="width:5.12619in;height:3.97844in" alt="A screenshot of a graph Description automatically generated" />
</figure>

## Step 5: Chassis Metrics

The important metrics of a chassis are the Fan Speeds, and Power consumption.

Select Chassis on the left and select a Chassis.

Click on Metrics.

For the chassis there are 28 metrics.

See what metrics are useful for you.

<figure>
<img src="assets/media/image232.png" style="width:7in;height:3.4in" alt="A screenshot of a computer Description automatically generated" />
</figure>

## Step 6: Fabric Interconnect Metrics

Metrics for the Fabric Interconnect include thermals, power consumption, memory utilization and more. Navigate to the **Operate / Fabric Interconnects** section on the left and select a Fabric Interconnect.

Click on Metrics.

<figure>
<img src="assets/media/image233.png" style="width:7in;height:3.79in" alt="A screenshot of a computer Description automatically generated" />
</figure>

At the top, select **Network Metrics**

**The values of the network metrics are in Bps (Bytes per second) and not bps (bits per second).**

<figure>
<img src="assets/media/image234.png" style="width:7in;height:1.42in" alt="A screenshot of a computer Description automatically generated" />
</figure>

## Step 7: Explorer

Intersight Metrics Explorer empowers you to aggregate and visualize various metrics that are collected for Fabric Interconnects, Chassis, and Servers that are managed as Intersight Managed Mode (IMM) or UCSM Managed Mode (UMM) domain in Cisco Intersight. You can use the Metrics Explorer queries to monitor your devices, optimize performance, identify bottlenecks, and proactively address any potential issues.

Navigate to the **Analyze /** **Explorer** menu on the left side**.**

<figure>
<img src="assets/media/image235.png" style="width:2.22222in;height:0.93936in" alt="A black and white text Description automatically generated" />
</figure>

Keep in mind, when you have the Advantage License Tier option, the data is collected every minute, but the granularity is still at 10 min.

![](assets/media/image237.png)

For the first metrics, we are selecting **Host Power and Status – Host Power – Maximum**

<figure>
<img src="assets/media/image238.png" style="width:7in;height:5.37in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Add a filter.
**Select Hostname and then Contains**.
Instead of selecting one device, click in the field and type: **RTP91-FI6454-05-1**(And hit enter)

<img src="assets/media/image239.png" style="width:4.99381in;height:3.03136in" alt="A screenshot of a computer AI-generated content may be incorrect." />

Click on “Group By” and select **Host Name**

Select a time interval of Last Month to see nicer graphs.

Here is the current result:

<figure>
<img src="assets/media/image240.png" style="width:7.51389in;height:3.92986in" alt="A screenshot of a computer AI-generated content may be incorrect." />
</figure>

lIf you want to have only the Top 5 shown, set the limit to 5

<figure>
<img src="assets/media/image241.png" style="width:5.86745in;height:1.13212in" alt="A screenshot of a computer AI-generated content may be incorrect." />
</figure>

<figure>
<img src="assets/media/image242.png" style="width:4.79134in;height:2.56261in" alt="A screen shot of a graph AI-generated content may be incorrect." />
</figure>

**Disable** this metric (Slide next to “**Host Power – Maximum**” and **Add Metric** for a new metric.

<figure>
<img src="assets/media/image243.png" style="width:2.21686in;height:0.35836in" />
</figure>

Select **Network Interface – Operational Link Speed – Maximum**

Filter by: **Host Type equals Fabric Interconnect**

Group by: **Host Name**

Limit: **5**.

<figure>
<img src="assets/media/image244.png" style="width:4.41319in;height:3.10497in" alt="A screenshot of a computer AI-generated content may be incorrect." />
</figure>

The result you see are in Bps (Bytes per Second.)
This is for every network related metric. Keep this in mind that it is NOT bps (bits per second.)

In this case the Max link is 25 GBps or 200 Gbps.

<figure>
<img src="assets/media/image245.png" style="width:5.45466in;height:2.86597in" alt="A screenshot of a video AI-generated content may be incorrect." />
</figure>

To find the power usage of one chassis, you need to know the chassis identifier.

<figure>
<img src="assets/media/image246.png" style="width:5.76273in;height:3.04589in" alt="A screenshot of a computer Description automatically generated" />
</figure>

One easy way to get this, is to go to the Chassis you want to know the details and select metrics.

Go to Chassis / Select a Chassis / Click Metrics.

Look for the Power with PSU1 as Endpoint.

Expand it and click on **View in Explorer**

<figure>
<img src="assets/media/image247.png" style="width:7.90972in;height:2.39583in" alt="A screenshot of a computer Description automatically generated" />
</figure>

In Explorere you will see Power- Average, Power-Minimum and Power- Maximum.

Delete the first two by clicking on the garbage bin.

Click on **Filter By** and you will see;

<figure>
<img src="assets/media/image248.png" style="width:6.03819in;height:3.04767in" alt="A screenshot of a computer Description automatically generated" />
</figure>

The right Identifier is now chosen, but there is only one PSU and we want to have all PSUs to see the power consumption of the chassis.

Remove the Name = PSU1 and type in that field Name. Then select name and select contains.

<figure>
<img src="assets/media/image249.png" style="width:4.9728in;height:2.14151in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Instead of choosing a PSU from the list, type PSU and hit enter.

<figure>
<img src="assets/media/image250.png" style="width:4.83779in;height:2.68935in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Now you see the power consumption of the total chassis.

<figure>
<img src="assets/media/image251.png" style="width:9.46482in;height:3.24349in" alt="A screenshot of a computer Description automatically generated" />
</figure>
