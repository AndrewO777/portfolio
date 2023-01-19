<script>
</script>
<template>
<nav id="navbar">
	<ul>
		<li @click="$emit('about-clicked')">About me</li>
		<li @click="$emit('projects-clicked')">Projects</li>
		<li @click="$emit('project-downloads-clicked')">Project Downloads</li>
		<li @click="$emit('contact-clicked')">Contact Me</li>
	</ul>
</nav>
</template>
