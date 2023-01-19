<script>
	export default {
		data() {
			return {
				img: false
			}
		},
		methods: {
			ImageClicked(){
				this.img = !this.img;
				console.log("works");
			}
		}
	}
</script>
<template>
<div v-if="img">
	<img class="popupImage" src="/neofetch2.png">
	<button @click="ImageClicked">Close me</button>
</div>
<div v-if="!img">
<h2>About me</h2>
<hr/>
<p>Hi, I'm Andrew. I am a programmer, specifically a web developer. I know many programming languages and frameworks for example: Vue (which I built this site with), React, Svelte, JavaScript, HTML, CSS, C++, C#, Python, Java, Xamarin.Forms, Unity and Node.js. I also use am very familiar with Apache, NGINX and Linux. I actually use Arch linux as my desktop's operating system, but I've used many other distros like Gentoo and Ubuntu, this server is actually running on an Ubuntu server right now.</p>
<img src="/neofetch2.png" class="images" alt="Neofetch of my desktop with Gentoo Linux" @click="ImageClicked">
<p class="image_text">This is a neofetch of my desktop when I was using Gentoo Linux</p>
<p>I am currenting working as an independent contractor developing mobile apps with a team. The apps I am working on at the moment are Montjoy and Linguicity. Montjoy is not currently available but will be soon. I also play many intruments such as guitar, bass, drums, piano, cello, etc. I play in a band as the lead guitarist. For more information about the projects I've worked on check out the projects page.</p>
</div>
</template>
