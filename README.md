<h2>OpenBlock-MaconECD</h2>
A downtown development concept.
Think of each page as a brochure for that neighborhood.

<img src="http://i.imgur.com/FxCtT.png"/>

Macon: imported Zipcodes, Opportunity Zones, and Tax Abatement Districts

<h3>Based on OpenBlock</h3>
See <a href="http://demo.openblockproject.org">OpenBlock Demo</a>
and <a href="https://github.com/openplans/openblock">OpenBlock GitHub repo</a>.

<h3>Mobile Layout</h3>
Began work on a one-column, mobile-friendly layout. Replace "locations" in the URL with "mobile".

<a href="http://ec2-75-101-172-4.compute-1.amazonaws.com/mobile/zones/downtown-industrial-dist/">Mobile Page</a>

<h3>Integrates ArcGIS</h3>
Cities often use Esri's ArcGIS platform to store and share their geodata.
<br/>
Integration with that platform allows us to combine government data and social media.
<br/>
- This version of OpenBlock replaces OpenLayers maps with Esri's ArcGIS JavaScript API.
<br/>
- Tie a neighborhood to an ArcGIS Online web map by setting the Description to a web map ID
<br/>
- Import an ArcGIS Online web map onto any neighborhood view by adding &webmap=[ID] to any page URL
<img src="http://i.imgur.com/o7ZBv.png"/>
<br/>
- Restyle with watercolor maps by adding &watercolor=true to any page URL

<h3>Install</h3>
This repo contains changes made to the Amazon EC2 AMI.

Follow directions for setting up OpenBlock on EC2:<br/>
http://openblockproject.org/docs/install/aws.html

Use these commands to quickly replace a file on EC2:

    mv base.html base_original.html

    nano base.html

[paste in the source code]

[Ctrl X]<br/>
[Y]<br/>
[Enter]<br/>

When finished, enter this into the terminal to update the server:

touch /home/openblock/openblock/wsgi/myblock.wsgi