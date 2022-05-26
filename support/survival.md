---
layout: support
title: Survival server
permalink: /support/survival/
---

<section id="survivalServer">
	<div class="page-header">
		<h1>Survival server</h1>
	</div>
	<p>We have a survival server hosted on <code>survival.aedi.app</code> that acts as an extension of the creative server, a side project, which anyone can join.  It's based off a high-scale map of the Earth with nation's borders intact and uses the Factions plugin (formerly Towny) for players to claim chunks of land.</p>
	<h3>Factions basics</h3>
	<p>The operative goal of our survial extension is to establish competitiveness while remaining fun. It costs $100 in-game currency to start a faction using <code>/f create &lt;name&gt;</code> however chunks of land start at $25 in-game currency and that cost will increase per each additionally claimed piece of land: <code>25 + (25 * 0.025 * ownedLand)</code>.</p>
	<p>Relations between factions default to neutral, however this can be changed. The <b>ally</b> and <b>truce</b> relations require a mutual agreement to take effect (via commands) however the <b>enemy</b> relation is one-sided and does not require any form of consent on behalf of the receiving party. Factions have a permissions structure that allow for factions owners to control particular aspects of the plugin as they trickle down to players within a faction.</p>
	<p>Each faction has its own bank or vault that can be managed with the command <code>/f money</code> that in turn provides a list of money-related commands.  In-game currency from your own <code>/balance</code> must be deposited into the faction's bank so that certain things can be paid for, including land.</p>
	<h4>List of survival commands</h4>
	<p>This is a shortened list of commands that are helpful for the survival server, having to do with Factions.  The <code>/f help</code> list should be referred to, as many commands have been intentionally excluded from this list.</p>
	<table class="table table-bordered table-striped">
		<thead>
			<tr>
				<th>Syntax</th>
				<th>Description</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td><code>/f help</code></td>
				<td>Displays a list of commands for Factions.</td>
			</tr>
			<tr>
				<td><code>/f money [...]</code></td>
				<td>Displays a list of money-related commands for Factions.</td>
			</tr>
			<tr>
				<td><code>/f list</code></td>
				<td>Displays a list of active factions on the server.</td>
			</tr>
			<tr>
				<td><code>/f show</code><code>/f who</code></td>
				<td>Displays a summary of your faction's current status.</td>
			</tr>
			<tr>
				<td><code>/f join &lt;faction&gt;</code></td>
				<td>Lets you join a faction.</td>
			</tr>
			<tr>
				<td><code>/f home</code></td>
				<td>Teleports you to your faction's home.</td>
			</tr>
			<tr>
				<td><code>/f create &lt;name&gt;</code></td>
				<td>Creates a new faction.</td>
			</tr>
			<tr>
				<td><code>/f description &lt;desc&gt;</code></td>
				<td>Changes the faction's description.</td>
			</tr>
			<tr>
				<td><code>/f rename &lt;tag&gt;</code></td>
				<td>Changes the faction's tag (name).</td>
			</tr>
			<tr>
				<td><code>/f open [yes/no=flip]</code></td>
				<td>Toggles if the faction requires an invitation to join.</td>
			</tr>
			<tr>
				<td><code>/f sethome</code></td>
				<td>Marks the faction's home.</td>
			</tr>
		</tbody>
	</table>
	<h3>Voting for the server</h3>
	<p>Casting a vote in favor of the server on a number of gameserver listing websites will give you benefits.  Each player is given $1,000 in-game currency by the server in exchange for their vote.  Below are a number of websites you may vote on that will be recognized.</p>
	<table class="table table-bordered table-striped">
		<thead>
			<tr>
				<th>#</th>
				<th>Server listing</th>
				<th>URL redirect</th>
			</tr>
		</thead>
		<tbody>
			<tr>
				<td>1</td>
				<td>TopG</td>
				<td><a href="/vote/topg" target="_blank">https://aedi.app/vote/topg/</a></td>
			</tr>
			<tr>
				<td>2</td>
				<td>Planet Minecraft</td>
				<td><a href="/vote/pmc" target="_blank">https://aedi.app/vote/pmc/</a></td>
			</tr>
			<tr>
				<td>3</td>
				<td>Minecraft-Server-List</td>
				<td><a href="/vote/mcl1" target="_blank">https://aedi.app/vote/mcl1/</a></td>
			</tr>
			<tr>
				<td>4</td>
				<td>MinecraftServers</td>
				<td><a href="/vote/ms1" target="_blank">https://aedi.app/vote/ms1/</a></td>
			</tr>
		</tbody>
	</table>
	<h3>Dynamic map</h3>
	<p>There is a dynamic map generated with Dynmap and hosted on <code>survival.aedi.app</code> <a href="https://survival.aedi.app/" target="_blank">in your browser</a>.  This is exclusive to the survival extension and may load slower than the static map generated with Mapcrafter or may not be served at all if the server is offline.</p>
</section>
