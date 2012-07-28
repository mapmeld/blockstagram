<h2>Blockstagram</h2>
A downtown development concept based on OpenBlock and ArcGIS Online.

Connect Blockstagram to an ArcGIS Shapefile or FeatureLayer to create a social media brochure for each block, economic development district, or neighborhood board.

Add an official Instagram account and partner services to promote official content.

<h3>Sample</h3>
Macon, GA: imported Zipcodes, Opportunity Zones, and Tax Abatement Districts for downtown

<img src="http://i.imgur.com/E3yDA.png"/>

<h3>Based on OpenBlock</h3>
See <a href="http://demo.openblockproject.org">OpenBlock Demo</a>
and <a href="https://github.com/openplans/openblock">OpenBlock GitHub repo</a>.

You can set up OpenBlock on Amazon EC2 or your own Ubuntu web server. It comes with several services to import local MeetUps and social media content.

<h3>Mobile Layout</h3>
Replace "locations" in the OpenBlock URL with "mobile" to see a single-column layout.

<a href="http://ec2-23-20-172-37.compute-1.amazonaws.com/mobile/zones/downtowntest2/">Mobile Page</a>

<h3>Integrates ArcGIS</h3>
Cities often use Esri's ArcGIS platform to store and share their geodata. Integration with this platform allows us to combine government data and social media.
<br/>
- (todo) Set up the map of city blocks, neighborhoods, or districts from a shapefile, Feature Layer, or Feature Service.
<br/>
- This version of OpenBlock replaces OpenLayers maps with Esri's ArcGIS JavaScript API.
<br/>
- Tie a neighborhood to an ArcGIS Online web map by setting the Description to a web map ID
<br/>
- Import an ArcGIS Online web map onto any neighborhood view by adding &webmap=[ID] to any page URL
<img src="http://i.imgur.com/o7ZBv.png"/>

<h3>Ideas</h3>
- Include official Flickr accounts
<br/>
- Better control over adding anonymous users photos
<br/>
- Only add photos with faces using PyFaceDetect

<h3>Install</h3>
This repo contains changes made to the Amazon EC2 AMI.

Follow directions for setting up OpenBlock on EC2:<br/>
http://openblockproject.org/docs/install/aws.html

Use these commands to quickly replace a file on EC2:

    mv base.html base_original.html

    nano base.html

[paste in the new code for base.html]

[Ctrl X]<br/>
[Y]<br/>
[Enter]<br/>

When finished, enter this into the terminal to update the server:

    touch /home/openblock/openblock/wsgi/myblock.wsgi