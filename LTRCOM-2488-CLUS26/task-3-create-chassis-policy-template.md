# Task 3: Create Chassis Policy Template

To create a Chassis Profile Template, Go to **Templates**, **UCS Chassis Profile Template**, and click **Create UCS Chassis Profile Template**:

<figure>
<img src="assets/media/image93.png" style="width:5.16304in;height:2.41926in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Provide a name, set the tag, and click **Next**:

<figure>
<img src="assets/media/image94.png" style="width:3.15179in;height:2.35365in" alt="A screenshot of a computer program Description automatically generated" />
</figure>

Create a new IMC Access Policy by clicking **Select Policy** next to IMC Access and then click **Create Policy**. Provide a name, set the tag, and click **Next**:

<figure>
<img src="assets/media/image95.png" style="width:2.65226in;height:2.12282in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Select the **UCS Chassis** tab, change the VLAN ID to **70,** click **Select IP Pool** under IP Pool, select the **UCSXKVMPool** radio button from the list, press **Select**, then press **Create:**

<figure>
<img src="assets/media/image96.png" style="width:3.08865in;height:2.47005in" alt="A screenshot of a computer AI-generated content may be incorrect." />
</figure>

**Best practice:**

- Every chassis do need two IP addresses from a pool. Create a separate Chassis-IP-Pool which is non overlapping with other IP Pools

Create a new Power Policy by clicking **Select Policy** next to **Power** and then click **Create Policy**. Provide a name, set the tag, and click **Next**:

<figure>
<img src="assets/media/image97.png" style="width:2.51532in;height:1.89115in" alt="A screenshot of a computer program Description automatically generated" />
</figure>

Select **UCS Chassis**, ensure **Grid** is selected for the Power Redundancy Policy, and click **Create**:

<figure>
<img src="assets/media/image98.png" style="width:2.77173in;height:2.23451in" alt="A screenshot of a computer AI-generated content may be incorrect." />
</figure>

**Best Practices**

- Redundancy per customer requirements

- Default options recommended for others

- Dynamic power rebalancing will re-allocate power between servers if competing for power in power constrained environments.

- Power allocation sets an input power limit. Throttling is used to stay within the limit.

Create a new Chassis SNMP Policy by clicking **Select Policy** next to **SNMP** and then click **Create Policy**. Provide a name, set the tag, and click **Next**:

<figure>
<img src="assets/media/image99.png" style="width:2.62301in;height:2.02893in" alt="A screenshot of a computer program Description automatically generated" />
</figure>

Select **UCS Chassis,** type **ACString** in the Access Community String, and click **Create**:

<figure>
<img src="assets/media/image100.png" style="width:3.36031in;height:2.06758in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Create a new Chassis Thermal Policy by clicking **Select Policy** next to **Thermal** and then click **Create Policy**. Provide a name, set the tag, and click **Next**:

<img src="assets/media/image101.png" style="width:2.49384in;height:1.8523in" alt="A screenshot of a computer program Description automatically generated" />.

**Best Practices**

- Applies to chassis or rack mount servers

- Sets the base fan speed

- Workloads with frequent transitions from idle to max may throttle while fan speeds ramp from lower levels.

- Increase policy to prevent throttling.

Select **UCS Chassis,** ensure **Balanced** is selected for the Fan Control Mode, and click **Create**.

<figure>
<img src="assets/media/image102.png" style="width:4.19996in;height:2.30756in" alt="A screenshot of a computer Description automatically generated" />
</figure>

After the creation of the policies, the chassis configuration should look similar to the image below. Click **Next** and **Close**. (Do NOT click Derive Profiles):

<figure>
<img src="assets/media/image103.png" style="width:4.13664in;height:1.57202in" alt="A screenshot of a computer Description automatically generated" />
</figure>
