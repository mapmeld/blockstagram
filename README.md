<h2>OpenBlock-MaconECD</h2>
A downtown development concept

Think of each page as a brochure for that neighborhood

<img src="http://imgur.com/FxCtT" width="400"/>

Imported Zipcodes, Opportunity Zones, and Tax Abatement Districts

<h3>Based on OpenBlock</h3>
See <a href="http://demo.openblockproject.org">OpenBlock Demo</a>
and <a href="https://github.com/openplans/openblock">OpenBlock GitHub repo</a>.

<h3>Integrates ArcGIS</h3>
Cities often use Esri's ArcGIS platform to store and share their geodata.
<br/>
Integration with that platform allows us to combine government data and social media.
<br/>
- This version of OpenBlock replaces OpenLayers maps with Esri's ArcGIS JavaScript API.
<br/>
- You can tie a neighborhood to an ArcGIS Online web map by setting the Description to a web map ID
<br/>
- You can show an ArcGIS Online web map with any neighborhood page by adding &webmap=[ID] to any neighborhood URL

<h3>Install</h3>
This repo contains changes made to the Amazon EC2 AMI.

Follow directions for setting up OpenBlock on EC2:<br/>
http://openblockproject.org/docs/install/aws.html

Use these commands to quickly replace a file on EC2:

<code>
mv base.html base_original.html
<br/>
nano base.html
</code>

[paste in the source code]

[Ctrl X]<br/>
[Y]<br/>
[Enter]<br/>
