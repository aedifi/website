---
layout: support
title: List of commands
permalink: /support/commands/
---

<section id="commandsList">
	<div class="page-header">
		<h1>List of commands</h1>
	</div>
	<p>This is a list of commands included in each of the three plugins used on the server.  They are organized by permission level of which there are four ranks: visitor (granted to every player when they join), architect, moderator and administrator.  Permissions are stored in a <code>Ranks.sqlite</code> file which also contains each player's rank according to their UUID.</p>
	<p><code>/help</code> can be used in-game or from console to list permissible commands.</p>
	<div class="alert alert-info">
		<strong>Heads up!</strong> This page is a work in progress, so it may be incomplete or misleading. It's also only relevant to the <b>creative server</b>.
	</div>
	<h4>Visitor-level commands</h4>
	<table class="table table-bordered table-striped">
		<thead>
			<tr>
				<th>Syntax</th>
				<th>Permission(s)</th>
				<th>Description</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td><code>/ascend</code></td>
				<td><code>edits.navigation.ascend</code></td>
				<td>Ascends you upward.</td>
			</tr>
			<tr>
				<td><code>/biomes</code></td>
				<td><code>edits.biomes</code></td>
				<td>Lists biomes compatible with the server.</td>
			</tr>
			<tr>
				<td><code>/chunks</code></td>
				<td><code>basics.chunks</code></td>
				<td>Lists any chunks in the server's memory.</td>
			</tr>
			<tr>
				<td><code>/commands</code> <code>/help</code></td>
				<td><code>basics.help</code></td>
				<td>Lists permissible commands.</td>
			</tr>
			<tr>
				<td><code>/cui</code></td>
				<td><code>edits.cui</code></td>
				<td>Completes the CUI visualizer handshake.</td>
			</tr>
			<tr>
				<td><code>/descend</code></td>
				<td><code>edits.navigation.descend</code></td>
				<td>Descends you downward.</td>
			</tr>
			<tr>
				<td><code>/distance &lt;distance&gt;</code></td>
				<td><code>basics.distance</code></td>
				<td>Sets your render distance. `distance` = `min - max` for client.</td>
			</tr>
			<tr>
				<td><code>/formats</code></td>
				<td><code>edits.schematic.list</code></td>
				<td>Lists supported schematic formats.</td>
			</tr>
			<tr>
				<td><code>/lag</code></td>
				<td><code>basics.lag</code></td>
				<td>Calculates the server's average t/s.</td>
			</tr>
			<tr>
				<td><code>/players</code></td>
				<td><code>basics.players</code></td>
				<td>Lists players who are online.</td>
			</tr>
			<tr>
				<td><code>/plugins</code></td>
				<td><code>basics.plugins</code></td>
				<td>Lists plugins installed/enabled on the server.</td>
			</tr>
			<tr>
				<td><code>/ranks</code></td>
				<td><code>basics.ranks</code></td>
				<td>Lists configured ranks.</td>
			</tr>
			<tr>
				<td><code>/memory</code></td>
				<td><code>basics.memory</code></td>
				<td>Calculates the amount of memory being used.</td>
			</tr>
			<tr>
				<td><code>/motd</code></td>
				<td><code>basics.motd</code></td>
				<td>Displays the message of the day.</td>
			</tr>
			<tr>
				<td><code>/nearby</code></td>
				<td><code>basics.nearby</code></td>
				<td>Lists players who are nearby.</td>
			</tr>
			<tr>
				<td><code>/worlds</code></td>
				<td><code>basics.worlds</code></td>
				<td>Lists configured worlds.</td>
			</tr>
			<tr>
				<td><code>/whisper &lt;player&gt; &lt;message&gt;</code> <code>/reply &lt;message&gt;</code></td>
				<td><code>basics.whisper</code></td>
				<td>Directly messages somebody.</td>
			</tr>
			<tr>
				<td><code>/schematics</code></td>
				<td><code>edits.schematic.list</code></td>
				<td>Lists schematics on the server.  Because there are so many, it will just link you to the <a href="https://files.aedi.app/schematics/" target="_blank">file server</a>.</td>
			</tr>
			<tr>
				<td><code>/seed [world]</code></td>
				<td><code>basics.seed</code></td>
				<td>Displays the world's seed.</td>
			</tr>
			<tr>
				<td><code>/spawn [world]</code></td>
				<td><code>basics.spawn</code></td>
				<td>Takes you to any world's spawn.</td>
			</tr>
		</tbody>
	</table>
</section>
