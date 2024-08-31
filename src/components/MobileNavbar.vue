<script>
export default {
    data() {
        return {
            showLinks: false,
        }
    },
    methods: {
        ShowLinks(){
            this.showLinks = !this.showLinks;
        }
    }
}
</script>
<template>
<nav id="mobile-navbar" style="margin-top:1em;margin-bottom:.8em;">
    <div id="title" style="display:inline-block;width:190px;margin:0;padding:0;">
        <h1 style="line-height:0;">Andrew Odom</h1>
    </div>
    <div class="nav-button" @click="ShowLinks">
        <div style="background-color: #777;border-radius:20px;width:30px;height:4px;margin-top:4px;margin-bottom:4px;margin-left:auto;margin-right:auto;"></div>
        <div style="background-color: #777;border-radius:20px;width:30px;height:4px;margin-top:4px;margin-bottom:4px;margin-left:auto;margin-right:auto;"></div>
        <div style="background-color: #777;border-radius:20px;width:30px;height:4px;margin-top:4px;margin-bottom:4px;margin-left:auto;margin-right:auto;"></div>
    </div>
	<ul v-if="showLinks">
		<li class="nav-mobile-link" @click="$emit('about-clicked')">About me</li>
		<li class="nav-mobile-link" @click="$emit('projects-clicked')">Projects</li>
		<li class="nav-mobile-link" @click="$emit('project-downloads-clicked')">Project Downloads</li>
		<li class="nav-mobile-link" @click="$emit('contact-clicked')">Contact Me</li>
	</ul>
</nav>
</template>
