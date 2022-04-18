---
layout: default
title: Index
permalink: /
---

<div class="jumbotron padded">
	<h1>A semi-whitelisted building server for Minecraft.</h1>
	<p class="lead">Aedificum is a lightweight building server with a whole bunch of cool features. It runs Cuberite, a FOSS alternative to Bukkit written in C++ and can perform large block operations without using too much memory.</p>
	<a class="btn btn-large applyBuild" id="btn-left" href="/apply" data-toggle="tooltip" data-placement="bottom" title data-original-title="Become an architect on the creative server!">Apply to build</a>
	<a class="btn btn-large btn-success joinDiscord" id="btn-right" href="/guild" data-toggle="tooltip" data-placement="bottom" title data-original-title="Join our Discord server to connect with other players!">Chat with us</a>
</div>
<!-- Embedded gameserver map -->
<div class="hero-unit">
	<!-- world_classic -> surface & zoom -> 6 & x -> 0, z -> 16, y -> 64 -->
	<iframe src="https://map.aedi.app/#world_classic/0/6/0/16/64"></iframe>
</div>
<!-- Tooltips -->
<script>
$(function() {
	$('.applyBuild').tooltip();
	$('.joinDiscord').tooltip();
});
</script>
