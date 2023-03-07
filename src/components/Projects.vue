<script>
export default{
	data(){
		return {
			cultpopup: false,
			montjoySearchPopup: false,
			chatapppopup: false
		}
	},
	methods: {
		PopupImage(img){
			if (img == 0){
				this.cultpopup = !this.cultpopup;
			}
			else if (img == 1){
				this.montjoySearchPopup = !this.montjoySearchPopup;
			}
			else if (img == 2){
				this.chatapppopup = !this.chatapppopup;
			}
		}
	}
}
</script>
<template>
<div v-if="cultpopup">
	<img src="/cult.png" class="popupImage">
	<button @click="PopupImage(0)">Close me</button>
</div>
<div v-if="montjoySearchPopup">
	<img src="/montjoy_search.jpg" class="popupImage">
	<button @click="PopupImage(1)">Close me</button>
</div>
<div v-if="chatapppopup">
	<img src="/chatapp.png" class="popupImage">
	<button @click="PopupImage(2)">Close me</button>
</div>
<div v-if="!cultpopup && !montjoySearchPopup && !chatapppopup">
	<h2>Projects</h2>
	<hr/>
	<h3>Montjoy</h3>
	<p>Montjoy is the project I've spent the most time on. It is an app where you can request live video streams from the streamers registered with the app from anywhere. I added the video streaming and searching functionality to the app as well as a page where you can download the recordings of past streams. I also created a few of the pages in the app. The app was created with Xamarin.Forms the backend server is a Node server with Express and it uses a MySQL database.</p>
	<img @click="PopupImage(1)" src="/montjoy_search.jpg" class="images" style="width:25%; max-width: 300px;">
	<h3>Linguicity</h3>
	<p></p>
	<h3>Text-based Adventure Game</h3>
	<p>I made this game in C++ for a school project, the name of the game is Cult and the download is available on github the link is on the project downloads page. The game is a little bit like Zork, except I made it with random generation for all the enemies, items, rooms, and objects in the rooms. The game uses pointers for keeping track of the rooms. There are many classes for the different parts, for example, the player, enemies, items, the map, etc. </p>
	<img @click="PopupImage(0)" src="/cult.png" class="images">
	<h3>Chat App</h3>
	<p>I made a chat app in React Native and Firebase as the backend with <a href="https://github.com/cjl1197">Craig Lawyer</a> this app was built for a school project. The purpose of the app is to be a simple chat app where you can find users and directly message them with no ads and simplicity in mind.</p>
	<img @click="PopupImage(2)" src="/chatapp.png" class="images" style="width: 25%; max-width: 300px;">
</div>
</template>
