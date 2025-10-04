---
layout: default
title: Index
permalink: /
---

<div class="jumbotron index">
	<h1>A server for Minecraft where you can build anything you want.</h1>
	<p class="lead">Aedificium is a lightweight building server with a whole bunch of cool features. It runs Cuberite, a FOSS alternative to Bukkit written in C++ and can perform large block operations without using too much memory.</p>
	<div class="server-status frame">
		<div class="server-status indicator"></div><p class="server-status text">Obtaining server status...</p> <button type="button" class="btn">Refresh</button>
	</div>
	<div class="server-ip">
		<span>
			<label>In-game IP address:</label> <button type="button" class="btn" disabled="disabled">play.aedi.app</button> <button type="button" class="btn">Copy</button>
		</span>
	</div>
	<a class="btn btn-large btn-success joinDiscord" href="/guild" data-toggle="tooltip" data-placement="bottom" title data-original-title="Join our Discord server to connect with other players!"><img src="/assets/svg/discord_icon.svg" alt="Discord icon"> Join our Discord server</a>
	<div class="social-links"><span>
		<button type="button" class="btn">Default</button> <button type="button" class="btn">Default</button> <button type="button" class="btn">Default</button>
	</span></div>
	<div id="taper-filler"></div>
</div>
<div class="jumbotron taper"></div>
<!-- Tooltips -->
<script>
const statusIndicator = document.querySelector('.server-status.indicator');
const statusText = document.querySelector('.server-status.text');
MinecraftAPI.getServerStatus('play.aedi.app', function (error, server) {  
	if (error) {
		statusIndicator.classList.add('offline');
		statusText.innerHTML = 'Unable to obtain server status.';
		return;
	}
	statusIndicator.classList.add(server.online ? 'online' : 'offline');
	statusText.innerHTML = 'The server is currently <b>' + (server.online ? 'online' : 'offline') + '</b>';
	if (server.online && server.players.now) statusText.innerHTML += ' with ' + parseInt(server.players.now) + ' player' + (server.players.now > 1 ? 's' : '');
	statusText.innerHTML += '.';
});
</script>
