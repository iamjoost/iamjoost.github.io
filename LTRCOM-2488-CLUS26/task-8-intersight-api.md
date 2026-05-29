# Task 8: Intersight API

APIs are very useful for automation and get information quickly.

In this section we will go over the Intersight API Rest Client and how you can use it.

There are open-source applications, like **isctl** that can be used to create your own

Script/application.

## Step 1: Where to find the Intersight API Rest Client?

When you are loged in into Intersight, you can go to the Help Center.

<figure>
<img src="assets/media/image252.png" style="width:4.59066in;height:2.00413in" />
</figure>

Once you are at the Intersight Help Center, Scroll all the way down to the **Intersight Services”** and select API Documentation.

<figure>
<img src="assets/media/image253.png" style="width:7.90833in;height:1.90833in" alt="A screenshot of a computer Description automatically generated" />
</figure>

At the top bar, click **API reference** and here you will see the API Rest Client.

<figure>
<img src="assets/media/image254.png" style="width:7.91666in;height:0.34375in" />
</figure>

## Step 2: Getting Chassis Information

In this step you will see how you can get information out of the API.

Find the **equipment/Chssisidentities** by using the search bar. You will see scrolling to the list is time consuming.

<figure>
<img src="assets/media/image255.png" style="width:3.13194in;height:2.68931in" alt="A screenshot of a computer Description automatically generated" />
</figure>

When you open it, there are two the same get.
The top one is to get all information of all chassis in the tenant.
The second one is to get specific information of a chassis, but then you will have to know the MOID.

<figure>
<img src="assets/media/image256.png" style="width:2.94023in;height:3.32639in" alt="A screenshot of a chat Description automatically generated" />
</figure>

Select the top GET and make sure **REST Client** is enabled. When it is enabled, you will see the REST Client on the right.
Click **Send.**

<figure>
<img src="assets/media/image257.png" style="width:4.38048in;height:4.04306in" alt="A screenshot of a computer Description automatically generated" />
</figure>

When you see a “200 success” the API information is there.
You will see different MOID in the response and you will have to search for your chassis and MOID.
Search for Chassis you want to get more information and then copy that MOID number.

<img src="assets/media/image258.png" style="width:5.01389in;height:2.27418in" alt="A screen shot of a computer Description automatically generated" />

Go back to the left and now click on the second get:

<figure>
<img src="assets/media/image259.png" style="width:2.88884in;height:3.52778in" alt="A screenshot of a chat Description automatically generated" />
</figure>

With this get, you need the MOID that you just copied. Fill it in the {Moid} field.

<figure>
<img src="assets/media/image260.png" style="width:4.20833in;height:2.50842in" alt="A screenshot of a computer Description automatically generated" />
</figure>

The result is that you get only information about one chassis.

<figure>
<img src="assets/media/image261.png" style="width:5.32721in;height:6.87453in" alt="A screenshot of a computer program Description automatically generated" />
</figure>

## Step 3: Query Parameters

To get only the information you want to have, **Query Parameters** can be used.

Select the first “get” of the **equipment/Chassisidentities** and add a Query Paramter.
The Key is **\$select** and the Value is **Name, Serial**.
The Moid will be shown, eventhough it is not selected.

<img src="assets/media/image262.png" style="width:4.23988in;height:5.81944in" alt="A screenshot of a computer Description automatically generated" />

To show serial numbers and models of the servers connected to a particular Fabric Interconnect we are using the **Compute/PhysicalSummaries** API.
This will give you ideas how to use the query parameters.

Find this API in the search bar.

<figure>
<img src="assets/media/image263.png" style="width:3.03059in;height:4.26528in" alt="A screenshot of a web page Description automatically generated" />
</figure>

Select the first Get and add a Query Parameter.

Key: **\$select** and Value: **Name, Serial, Model**
Then add another Query Parameter:

Key; **\$filter** and Value: **startswith(Name,’RTP91-FI6454-03-1’)**

<figure>
<img src="assets/media/image264.png" style="width:3.64705in;height:6.21327in" alt="A screenshot of a computer program Description automatically generated" />
</figure>

## Step 4: Opensource tools

The Intersight REST API Client is great and it is possible to use other tools like isctl.
First you have to download it from : <https://github.com/cgascoig/isctl>

<figure>
<img src="assets/media/image265.png" style="width:3.53333in;height:2.09988in" alt="A screenshot of a computer Description automatically generated" />
</figure>

On the right side of the webpage, click on the latest release.

<figure>
<img src="assets/media/image266.png" style="width:2.57639in;height:1.17233in" alt="A screenshot of a chat Description automatically generated" />
</figure>

Download the windows version.

<figure>
<img src="assets/media/image267.png" style="width:2.79056in;height:1.79167in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Extract the file and copy the executable in a directory on the laptop.

<figure>
<img src="assets/media/image268.png" style="width:3.53333in;height:0.625in" alt="A blue rectangle with white border Description automatically generated" />
</figure>

Before you can use this application, you must have an API key of Intersight.

Go to **Intersight / Settings.**

<figure>
<img src="assets/media/image269.png" style="width:2.17231in;height:4.09683in" />
</figure>

Go to API Keys and generate an API Key for OpenAPI schema version 3. <img src="assets/media/image270.png" style="width:7.70834in;height:2.90625in" />

Give it a description and expiration date for the future.

<figure>
<img src="assets/media/image271.png" style="width:4.47269in;height:4.28555in" />
</figure>

When the API Key is generated, copy the API Key ID and download the secret key.
**Do not close this window, until you are certain the isctl application is working.**

<figure>
<img src="assets/media/image272.png" style="width:3.81754in;height:3.75694in" alt="A screenshot of a computer Description automatically generated" />
</figure>

Open the Command prompt in Windows (CMD)

And type: **isctl configure**

You will have to give the API Key ID and the location of the API secret key file.

<figure>
<img src="assets/media/image273.png" style="width:7in;height:3.83in" alt="A screenshot of a computer Description automatically generated" />
</figure>

<figure>
<img src="assets/media/image274.png" style="width:7in;height:1.18in" alt="A computer screen with white text Description automatically generated" />
</figure>

Once that is working, you can test it by typing the following command;
**isctl get ntp policy**

<figure>
<img src="assets/media/image275.png" style="width:7in;height:1.16in" alt="A screen shot of a computer Description automatically generated" />
</figure>

To get the same result as the step with the filter and select query paramer, you can type:
**isctl get compute physicalsummary --select "Name,Serial,Model" --filter "startswith(Name,'RTP91-FI6454-03-1')**

There are two **–** before select and filter parameter and it is case sensitive.

<figure>
<img src="assets/media/image276.png" style="width:6.88909in;height:1.41108in" alt="A screen shot of a computer Description automatically generated" />
</figure>

To have the output in a certain order, you can use -o Name

<figure>
<img src="assets/media/image277.png" style="width:6.98501in;height:1.27742in" alt="A black screen with white text Description automatically generated" />
</figure>

Different outputs are possible like yaml, json, csv, xlsx.

<figure>
<img src="assets/media/image278.png" style="width:6.93477in;height:1.61101in" alt="A black screen with white text Description automatically generated" />
</figure>

<figure>
<img src="assets/media/image279.png" style="width:6.92436in;height:1.17392in" alt="A black screen with white text Description automatically generated" />
</figure>
