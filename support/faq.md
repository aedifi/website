---
layout: support
title: Frequently asked questions
permalink: /support/faq/
---
Before asking for help with anything, you should read through this list of <b>frequently asked questions</b> and ensure that what you're asking hasn't already been addressed.

#### Is [insert version here] supported?
The Minecraft server offers several methods of interaction through various clients.  As mentioned in the about page it runs Cuberite, a free and open source (FOSS) server software.  Because of Cuberite's limitations the software only supports features from the <code>1.12.2 (340)</code> version/protocol at this time.  It runs behind a proxy and lets players connect with versions leading up to the latest <b>stable</b> release of Minecraft <b>Java Edition</b> (<a href="https://wiki.vg/Protocol_version_numbers" target="_blank">1.18.2, protocol 758</a>).

<b>Bedrock Edition</b> is also supported through the address <code>creative.aedi.app</code>, though you will need a Java account to connect.

#### Is there a map of the server?
<!-- Mapcrafter explanation -->
<p>The <a href="https://mapcrafter.org/" target="_blank">Mapcrafter</a> map renderer is used to display an isometric view of our worlds that is served with nginx.  Our maps are hosted on <code>map.aedi.app</code> <a href="https://map.aedi.app/" target="_blank">in your browser</a> and a cropped position of the creative spawnpoint is displayed in an iframe on this site's homepage.</p>
<!-- Dynmap explanation -->
<p>There is also a dynamic map generated with Dynmap and hosted on <code>survival.aedi.app</code> <a href="https://survival.aedi.app/" target="_blank">in your browser</a>.  This is exclusive to the survival extension and may load slower than the static map generated with Mapcrafter or may not be served at all if the server is offline.

#### Is my data sent to any other websites?
We receive a few details about your account from Mojang in the same way the Minecraft client itself does.  However, it only asks Mojang about your username, which they already have. This is required to verify users are valid, to get the case corrected username and to get the UUID that's required to recognize you if your name changes.

Everything on this website is self-hosted and we don't make use of any web tracking in order to collect your data.
