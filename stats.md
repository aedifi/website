---
layout: default
title: Server statistics
permalink: /stats/
---
<div class="content">
	<ul class="breadcrumb">
    	<li><a href="/">Index</a> <span class="divider">/</span></li>
        <li class="active">Server statistics</li>
    </ul>
	<table class="table table-bordered table-striped server-stats" style="margin-bottom:10px">
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
	<button type="button" class="btn copy refreshStatus" onclick="document.querySelector('.icon-refresh').classList.add('icon-spin'); document.getElementById('srv-data-status').innerHTML = 'Loading...'; document.getElementById('srv-row-status').className = 'warning'; document.getElementById('srv-data-online').innerHTML = 'Loading...'; document.getElementById('srv-row-online').className = 'warning'; document.getElementById('srv-data-error').innerHTML = 'Loading...'; document.getElementById('srv-row-error').className = 'warning'; document.getElementById('srv-data-server-name').innerHTML = 'Loading...'; document.getElementById('srv-data-server-protocol').innerHTML = 'Loading...'; document.getElementById('srv-data-players-max').innerHTML = 'Loading...'; document.getElementById('srv-data-players-now').innerHTML = 'Loading...'; document.getElementById('srv-data-last-updated').innerHTML = 'Loading...'; document.getElementById('srv-data-last-online').innerHTML = 'Loading...'; document.getElementById('srv-data-duration').innerHTML = 'Loading...'; setTimeout(() => {getServerStatus(); document.querySelector('.icon-refresh').classList.remove('icon-spin');},100);" style="float:right; margin-left:5px"> <i class="icon-refresh"></i> Refresh</button>
	<p>Server statistics are obtained using <a href="https://mcapi.us/" target="_blank">MinecraftAPI <i class="icon-external-link"></i></a> and require JavaScript to be enabled.</p>
</div>
<script>
function getServerStatus() {
	const statusText = document.querySelector('.server-status.text');
	MinecraftAPI.getServerStatus('play.aedi.app', function (error, server) {  
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
