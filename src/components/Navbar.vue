<script>
</script>
<template>
<nav id="navbar">
    <div id="title">
        <img src="/Logo.png" class="mylogo">
        <h1>Andrew Odom</h1>
    </div>
	<ul>
		<li @click="$emit('about-clicked')">About me</li>
		<li @click="$emit('projects-clicked')">Projects</li>
		<li @click="$emit('project-downloads-clicked')">Project Downloads</li>
		<li @click="$emit('contact-clicked')">Contact Me</li>
	</ul>
</nav>
</template>
