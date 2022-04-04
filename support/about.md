---
layout: support
title: About the server
permalink: /support/
---

<section id="aboutServer">
	<div class="page-header">
		<h1>About the server</h1>
	</div>
	<p>Aedificium is a semi-whitelisted architecture-oriented server for the sandbox video game Minecraft.  Anyone can join our server and explore what architects have built for themselves or apply for the position in order to get building.  There are three ranks on our server, discounting new players: architect, moderator, and administrator.  The rank of architect grants every permission that is not moderation-related on our server.</p>
		<dl class="dl-horizontal">
            <dt>July 21, 2013</dt>
            <dd>The server began operating as a sandbox community named Chromium where every player was given building permissions.</dd>
			<dd>We originally ran a fork of CraftBukkit and a modified release of TotalFreedomMod, created by Steven Lawson and Jerom van der Sar, to give players "operator" access.</dd>
			<dt>August 31, 2015</dt>
			<dd>Chromium's server was destroyed due to a data loss incident.</dd>
			<dd>I created a new server based off the same model with the name "shadow.ga."</dd>
			<dt>May 4, 2018</dt>
			<dd>The server went offline for ~1 year and it has since returned as a place for builders with a whitelist as Aedificium.</dd>
			<dt>May 1, 2020</dt>
			<dd>We switched from a fork of the CraftBukkit server software to Cuberite, a free and open source (FOSS) server software.</dd>
			<dd>Shortly after this happened the development of our own plugins began in order to provide features that were previously had.</dd>
		</dl>
	<h3>Defining the creative server</h3>
	<p>The Minecraft server offers several methods of interaction through various clients.  As mentioned in the about page it runs Cuberite, a free and open source (FOSS) server software.  Because of Cuberite's limitations the software only supports features from the <code>1.12.2 (340)</code> version/protocol at this time.  It runs behind a proxy and lets players connect with versions leading up to the latest <b>stable</b> release of Minecraft <b>Java Edition</b> (<a href="https://wiki.vg/Protocol_version_numbers" target="_blank">1.18.2, protocol 758</a>).</p>
	<p>Joining the creative server through a forced host can be accomplished with the address <code>creative.aedi.app</code>.  The <code>aedi.app</code> address will direct clients to the server they were last on and defaults to creative.  <b>Bedrock Edition</b> is also supported through this forced host, though you will need a Java account to connect.</p>
	<h4>Practical implications of Cuberite</h4>
	<p>Cuberite is written in C++ and generally handles better than the game's Java server.  Each world runs in a separate thread and the server can perform under stringent conditions without much performance loss.  There is a <a href="https://forum.cuberite.org/thread-1888.html" target="_blank">lengthy write-up</a> about the server's performance on another forum.</p>
	<p>Plugins are written in the high-level Lua programming language with an intermediary for scripting.  Each of our server's <code>/plugins</code> are open-source and are continually being updated to improve the experience. There are three plugins on the server; Basics: which provides "basic" commands, Extras: which provides ease-of-use features, and Edits: which emulates the toolset of WorldEdit.</p>
	<p>The Edits plugin is a fork of NiLSPACE/worldedit and bears similarity to sk89q's WorldEdit plugin for CraftBukkit.  It aims to have the same set of commands however it has no affiliation with that plugin.  The primary advantage of "Edits" is its performance because of the <a href="https://api.cuberite.org/cBlockArea.html" target="_blank">cBlockArea class</a> that is used to access chunks directly.  <b>.schematic</b> is a file format used by WorldEdit/MCEdit with which Edits is fully compliant.</p>
	<h3>Support the community</h3>
	<p>Our server is completely free for players and moderated by volunteers.  We rely on community contributions to help us improve and expand upon the server.</p>
	<ol>
		<li>If you're a developer capable of <b>C++ or Lua scripting</b> consider contributing to our open source plugins on GitHub.  This is the most efficient way to help us because we are in need of developers and your work can improve the experience.  There are lots of things to be added.</li>
		<li>No money is made off the server but it does cost a significant amount each month in order to pay for these services.  Donations are always gratefully received.  There are no in-game benefits for players who provide financial support because Aedificium is at its core a <b>free-to-play</b> platform.</li>
		<li>Join our <b><a href="/guild" target="_blank">Discord server</a></b> for an easy method of getting in touch with other players.  If you feel knowledgeable, you can also provide support to beginners.  We are also working on a <b>community forum</b> to talk about the organized growth of this server.</li>
		<li>Finally, if you enjoy the server then you should not feel hesitant to share it to your friends or post about Aedificium on social media.  More awareness leads to more engagement and therefore more activity, architects, and better contributions.</li>
	</ol>
</section>
