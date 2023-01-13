<script>
import About from "./components/About.vue"
import Navbar from "./components/Navbar.vue"
import Titlebar from "./components/Titlebar.vue"
import Projects from "./components/Projects.vue"
import Downloads from "./components/Downloads.vue"
import Contact from "./components/Contact.vue"
export default{
	components: {
		About,
		Navbar,
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
	<Titlebar/>
  </header>

  <main>
	<Navbar @projects-clicked="ProjectsClicked" @about-clicked="AboutClicked"
		@project-downloads-clicked="ProjectDownloadsClicked"
		@contact-clicked="ContactClicked"/>
	<div id="content">
		<About v-if="about"/>
		<Projects v-if="projects"/>
		<Downloads v-if="downloads"/>
		<Contact v-if="contact"/>
	</div>
  </main>
</template>
