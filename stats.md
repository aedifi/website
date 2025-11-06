---
layout: special
title: Server statistics
permalink: /stats/
---
Server statistics are gathered using MinecraftAPI.

<table class="table table-bordered table-striped server-stats">
	<thead>
		<tr>
			<th>Category</th>
			<th>Data</th>
			<th>Value</th>
		</tr>
	</thead>
	<tbody>
		<!-- Server status -->
		<tr id="srv-row-status" class="warning">
			<td rowspan="3">Server status</td>
			<td>status</td>
			<td id="srv-data-status" class="value">Loading...</td>
		</tr>
		<tr id="srv-row-online" class="warning">
			<td>online</td>
            <td id="srv-data-online" class="value">Loading...</td>
        </tr>
		<tr id="srv-row-error" class="warning">
            <td>error</td>
            <td id="srv-data-error" class="value">Loading...</td>
        </tr>
		<!-- Minecraft protocol -->
		<tr>
			<td rowspan="2">Minecraft protocol</td>
			<td>server.name</td>
			<td id="srv-data-server-name" class="value">Loading...</td>
		</tr>
		<tr>
			<td>server.protocol</td>
			<td id="srv-data-server-protocol" class="value">Loading...</td>
		</tr>
		<!-- Player information -->
		<tr>
			<td rowspan="2">Player information</td><td>players.max</td>
			<td id="srv-data-players-max" class="value">Loading...</td>
		</tr>
		<tr>
			<td>players.now</td>
			<td id="srv-data-players-now" class="value">Loading...</td>
		</tr>
		<!-- Time -->
		<tr>
			<td rowspan="3">Time</td>
			<td>last_updated</td>
			<td id="srv-data-last-updated" class="value">Loading...</td>
		</tr>
		<tr>
			<td>last_online</td>
			<td id="srv-data-last-online" class="value">Loading...</td>
		</tr>
		<tr>             
			<td>duration</td>
			<td id="srv-data-duration" class="value">Loading...</td>
		</tr>
	</tbody>
</table>
<button type="button" class="btn copy" style="float:right; margin-bottom:5px"> <i class="icon-refresh"></i> Refresh</button>
<script>
function getServerStatus() {
	const statusText = document.querySelector('.server-status.text');
	MinecraftAPI.getServerStatus('play.aedi.app', function (error, server) {  
		if (error) {
			statusIndicator.classList.add('offline');
			statusText.innerHTML = 'Unable to obtain server status.';
			return;
		}
		// Populate values:
		// Server status
		document.getElementById('srv-data-status').innerHTML = '\"' + server.status + '\"';
		document.getElementById('srv-row-status').classList.remove('warning');
		if (server.status = 'success') document.getElementById('srv-row-status').classList.add('success');
		else document.getElementById('srv-row-status').classList.add('error');
		document.getElementById('srv-data-online').innerHTML = (server.online ? 'true' : 'false');
		document.getElementById('srv-row-online').classList.remove('warning')
		if (server.online) document.getElementById('srv-row-online').classList.add('success');
		else document.getElementById('srv-row-online').classList.add('error');
		document.getElementById('srv-data-error').innerHTML = (server.error ? '\"' + server.error + '\"' : 'null');
		if (server.error) {
			document.getElementById('srv-row-error').classList.remove('warning');
			document.getElementById('srv-row-error').classList.add('error');
		}
		// Minecraft protocol
		document.getElementById('srv-data-server-name').innerHTML = '\"' + server.server.name + '\"';
		document.getElementById('srv-data-server-protocol').innerHTML = server.server.protocol;
		// Player information
		document.getElementById('srv-data-players-max').innerHTML = server.players.max;
		document.getElementById('srv-data-players-now').innerHTML = server.players.now;
		// Time
		document.getElementById('srv-data-last-updated').innerHTML = server.last_updated;
		document.getElementById('srv-data-last-online').innerHTML = (server.last_online ? server.last_online : 'null');
		document.getElementById('srv-data-duration').innerHTML = server.duration;
	});
};
getServerStatus();
</script>
