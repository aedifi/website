---
layout: default
title: Index
permalink: /
---
<div class="jumbotron index">
	<!-- 10-4-25 alert -->
	<div class="alert alert-index"><button type="button" class="close" data-dismiss="alert alert-index">×</button><i class="icon-info-sign icon-2x figure"></i><strong>Returning players:</strong> On July 9 2025, the server shut down after suffering a power surge incident.  Two months later, on September 12, the server was brought back online.  Thanks to integral recovery efforts, there has been no data loss whatsoever.  <a href="/blog/2025/09/12/server-back-online">Read more »</a></div>
	<!-- End alert -->
	<h1>A server for Minecraft where you can build anything you want.</h1>
	<p class="lead">Aedificium is a lightweight building server with a whole bunch of cool features. It runs Cuberite, a FOSS alternative to Bukkit written in C++ and can perform large block operations without using too much memory.</p>
	<div class="server-status frame">
		<div class="server-status indicator"></div><p class="server-status text">Obtaining server status...</p> <button type="button" class="btn btn-mini refreshStatus" onclick="document.querySelector('.server-status .icon-refresh').classList.add('icon-spin'); document.querySelector('.server-status.indicator').classList.remove('online','offline'); document.querySelector('.server-status.text').innerHTML = 'Obtaining server status...'; setTimeout(() => {getServerStatus(); document.querySelector('.server-status .icon-refresh').classList.remove('icon-spin');},100);"><i class="icon-refresh"></i></button>
	</div>
	<div class="server-ip">
		<span>
			<label>In-game IP address:</label> <button type="button" class="btn" disabled="disabled">play.aedi.app</button> <button type="button" class="btn copy" onclick="navigator.clipboard.writeText('play.aedi.app'); document.querySelector('.btn.copy').classList.add('active'); document.querySelector('.btn.copy').innerHTML = '<i class=\'icon-paste\'></i> Copied'; setTimeout(() => {document.querySelector('.btn.copy').classList.remove('active'); document.querySelector('.btn.copy').innerHTML = '<i class=\'icon-paste\'></i> Copy';},1000);"><i class="icon-paste"></i> Copy</button>
		</span>
	</div>
	<a class="btn btn-large btn-success joinDiscord" href="/guild" target="_blank" data-toggle="tooltip" data-placement="bottom" title data-original-title="Join our Discord server to connect with other players!"><img src="/assets/svg/discord_icon.svg" alt="Discord icon"> Join our Discord server <i class="icon-external-link" style="margin-left:5px"></i></a>
	<div class="social-links">
		<p id="discord-tos">By joining, you are subject to the <a href="https://discord.com/terms" target="_blank">terms and conditions <i class="icon-external-link"></i></a> of Discord, Inc.</p>
		<span>
			<a class="btn" href="https://github.com/aedifi" target="_blank"><i class="icon-github-alt"></i> GitHub <i class="icon-external-link"></i></a> <a class="btn" href="https://twitter.com/aedsrv" target="_blank"><i class="icon-twitter"></i> Twitter <i class="icon-external-link"></i></a> <div class="btn-group">
				<button class="btn dropdown-toggle" data-toggle="dropdown">More links <span class="caret"></span></button>
				<ul class="dropdown-menu" style="text-align:left">
					<li><a href="https://www.planetminecraft.com/member/aedifi" target="_blank">Planet Minecraft <i class="icon-external-link"></i></a></li>
					<li><a href="https://murgleis.com/services/aedi" target="_blank">murgleis.com <i class="icon-external-link"></i></a></li>
				</ul>
        	</div>
		</span>
	</div>
	<div id="taper-filler"></div>
</div>
<div class="jumbotron taper"></div>
<!-- Server status -->
<script>
function getServerStatus() {
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
};
getServerStatus();
</script>
