---
layout: default
title: Index
permalink: /
---

<div class="jumbotron index padded">
	<h1>A server for Minecraft where you can build anything you want.</h1>
	<p class="lead">Aedificium is a lightweight building server with a whole bunch of cool features. It runs Cuberite, a FOSS alternative to Bukkit written in C++ and can perform large block operations without using too much memory.</p>
	<a class="btn btn-large applyBuild" id="btn-left" href="/apply" data-toggle="tooltip" data-placement="bottom" title data-original-title="Become an architect on the creative server!">Apply to build</a>
	<a class="btn btn-large btn-success joinDiscord" id="btn-right" href="/guild" data-toggle="tooltip" data-placement="bottom" title data-original-title="Join our Discord server to connect with other players!">Chat with us</a>
	<div class="server-status frame">
		<div class="server-status indicator"></div><p class="server-status text">Obtaining server status...</p>
	</div>
</div>
<!-- Tooltips -->
<script>
$(function() {
	$('.applyBuild').tooltip();
	$('.joinDiscord').tooltip();
});
</script>
<script>
const statusIndicator = document.querySelector('.server-status.indicator');
const statusText = document.querySelector('.server-status.text');
MinecraftAPI.getServerStatus('play.aedi.app', function (error, server) {  
	if (error) {
		statusText.innerHTML = 'Unable to obtain server status.';
		return;
	}
	statusIndicator.classList.add(server.online ? 'online' : 'offline');
	statusText.innerHTML = 'The server is currently <b>' + (server.online ? 'online' : 'offline') + '</b>';
	if (server.online && server.players.now) statusText.innerHTML += ' with ' + parseInt(server.players.now) + ' player' + (server.players.now > 1 ? 's' : '');
	statusText.innerHTML += '.';
});
</script>
