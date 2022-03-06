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
	<p>The Edits plugin allows for architects to save, load, and index selections which are copied to a member's clipboard. <code>.schematic</code> is a file format used by WorldEdit/MCEdit with which our plugins are fully compliant.  Schematics created using versions of sk89q WorldEdit >=1.13 with the <code>.schem</code> format may be converted using <a href="https://puregero.github.io/SchemToSchematic/" target="_blank">this tool</a>.  Legacy schematics may still be indexed and loaded in by newer versions of the game.</p>
	<p>A direct link to a schematic file can be imported to the server with the command <code>//schem import &lt;link&gt;</code>.  If the file is archived or is in a container the command will not extract it.  There currently exists no limit to the amount of schematics stored on our server provided they each bear unique names as files cannot be overwritten or deleted from in-game.</p>
	<p>Worlds, schematics and our latest build of Cuberite are each served as static content in a directory on a <a href="https://files.aedi.app/" target="_blank">file server</a> so that our players may easily download them to their own machine.  These are "source files" and will provide an accurate list of all schematics on the server.</p>
	<h4>Static map</h4>
	<p>The <a href="https://mapcrafter.org/" target="_blank">Mapcrafter</a> map renderer is used to display an isometric view of our worlds that is served with nginx.  Our maps are hosted on <code>map.aedi.app</code> <a href="https://map.aedi.app/" target="_blank">in your browser</a> and a cropped position of the creative spawnpoint is displayed in an iframe on this site's homepage.
</section>
