---
layout: support
title: Support index
permalink: /support/
---

<section id="supportIndex">
	<div class="page-header">
		<h1>Support index</h1>
	</div>
	<p>Before asking for support, you should read through our documentation and ensure that what you're asking hasn't already been addressed.</p>
	<h4>Defining the creative server</h4>
	<p>The Minecraft server offers several methods of interaction through various clients.  As mentioned in the about page it runs Cuberite, a free and open source (FOSS) server software.  Because of Cuberite's limitations the software only supports features from the <code>1.12.2 (340)</code> version/protocol at this time.  It runs behind a proxy and lets players connect with versions leading up to the latest known release <code>1.18.1 (757)</code>.</p>
	<p>Joining the creative server through a forced host can be accomplished with the address <code>creative.aedi.app</code>.  The <code>aedi.app</code> address will direct clients to the server they were last on and defaults to creative.</p>
	<h4>Practical implications of Cuberite</h4>
	<p>Cuberite is written in C++ and generally handles better than the game's Java server.  Each world runs in a separate thread and the server can perform under stringent conditions without much performance loss.  There is a <a href="https://forum.cuberite.org/thread-1888.html" target="_blank">lengthy write-up</a> about the server's performance on another forum.</p>
	<p>Plugins are written in the high-level Lua programming language with an intermediary for scripting.  Each of our server's <code>/plugins</code> are open-source and are continually being updated to improve the experience. There are three plugins on the server; Basics: which provides "basic" commands, Extras: which provides ease-of-use features, and Edits: which emulates the toolset of WorldEdit.</p>
	<p>The Edits plugin is a fork of NiLSPACE/worldedit and bears similarity to sk89q's WorldEdit plugin for CraftBukkit.  It aims to have the same set of commands however it has no affiliation with that plugin.  The primary advantage of "Edits" is its performance because of the <a href="https://api.cuberite.org/cBlockArea.html" target="_blank">cBlockArea class</a> that is used to access chunks directly.</p>
	<h4>Importing and exporting builds</h4>
	<p>Players retain sole ownership and the right to access their builds which are uploaded to or created on our server.  Because of this, we offer easy methods for these works to be shared with the rest of our community.</p>
	<p>The Edits plugin allows for architects to save, load, and index selections which are copied to a member's clipboard. Schematics are a file format used by WorldEdit/MCEdit with which our plugins are fully compliant.</p>
</section>
<hr class="hidden">
