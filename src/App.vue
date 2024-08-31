<script>
import About from "./components/About.vue"
import Navbar from "./components/Navbar.vue"
import MobileNavbar from "./components/MobileNavbar.vue"
import Titlebar from "./components/Titlebar.vue"
import Projects from "./components/Projects.vue"
import Downloads from "./components/Downloads.vue"
import Contact from "./components/Contact.vue"
export default{
	components: {
		About,
		Navbar,
        MobileNavbar,
		Titlebar,
		Projects,
		Downloads,
		Contact,
	},
	data() {
		return {
			about: true,
			projects: false,
			downloads: false,
			contact: false
		}
	},
	methods: {
		AboutClicked() {
			this.about = true;
			this.projects = false;
			this.downloads= false;
			this.contact = false;
		},
		ProjectsClicked() {
			this.about = false;
			this.projects = true;
			this.downloads = false;
			this.contact = false;
		},
		ProjectDownloadsClicked() {
			this.about = false;
			this.projects = false;
			this.downloads = true;
			this.contact = false;
		},
		ContactClicked() {
			this.about = false;
			this.projects = false;
			this.downloads = false;
			this.contact = true;
		}
	}
}
</script>
<template>
  <header>
  </header>

  <main>
    <MobileNavbar @projects-clicked="ProjectsClicked" @about-clicked="AboutClicked" @project-downloads-clicked="ProjectDownloadsClicked" @contact-clicked="ContactClicked"/>
	<Navbar @projects-clicked="ProjectsClicked" @about-clicked="AboutClicked" @project-downloads-clicked="ProjectDownloadsClicked" @contact-clicked="ContactClicked"/>
    <!--<div style="height: 1em"></div>-->
	<div id="content">
		<!--<p>Link to subdomain <a href="https://rwd-examples.andrewodom.net">rwd-examples.andrewodom.net</a></p>
        <p>Link to accounting question game <a href="https://accounting-game.andrewodom.net">accounting-game.andrewodom.net</a></p>-->
        <!--Leaving that as a comment for future reference-->
		<About v-if="about"/>
		<Projects v-if="projects"/>
		<Downloads v-if="downloads"/>
		<Contact v-if="contact"/>
	</div>
  </main>
</template>
