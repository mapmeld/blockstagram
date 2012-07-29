<h2>Blockstagram</h2>
A downtown development concept based on OpenBlock and ArcGIS Online.

<h3>Does this sound like you?</h3>
<ul>
<li>Each of our neighborhoods is unique, and we could use an online brochure / pamphlet to show off each one.</li>
<li>We have opportunity zones for businesses to start in our city, but we don't have a site showing where those areas are.</li>
<li>We have a social media presence that we use to promote local businesses and events, but there's no way to see what happens in each neighborhood.</li>
<li>The GIS Department has maps of opportunities downtown, and we want to share that online with potential businesses.</li>
</ul>

<h3>Built with your photos and maps</h3>
Set up Blockstagram to create a social media brochure for each economic development district or neighborhood board.

Link to your official account on Twitter, Flickr, or Instagram.  Add local businesses' accounts, too!

Ask the city's GIS team for a FeatureService or a shapefile to create brochure pages for each of your city's neighborhoods.

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