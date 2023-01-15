<script>
export default{
	data(){
		return {
			download1popup: false,
			download2popup: false
		}
	},
	methods: {
		PopupImage(img){
			if (img == 0){
				this.download1popup = !this.download1popup
			} else if (img == 1) {
				this.download2popup = !this.download2popup
			}
		}
	}
}
</script>
<template>
<div v-if="download1popup">
	<img src="/download1.png" class="popupImage">
	<button @click="PopupImage(0)">Close me</button>
</div>
<div v-if="download2popup">
	<img src="/download2.png" class="popupImage">
	<button @click="PopupImage(1)">Close me</button>
</div>
<div v-if="!download1popup && !download2popup">
	<h2>Downloads</h2>
	<hr/>
	<p>To download the programs click on the link of the one you want to download, click correct version for your os on the releases tab.</p>
	<img @click="PopupImage(0)" src="/download1.png" style="width: 30%; margin-left: auto; margin-right: auto; display: block;">
	<p>then click on the file ending in .exe to download it.</p>
	<img @click="PopupImage(1)" src="/download2.png" style="width: 30%; margin-left: auto; margin-right: auto; display: block;">
	<h3><a href="https://github.com/AndrewO777">My github</a></h3>
	<h3><a href="https://github.com/AndrewO777/portfolio">This Website</a></h3>
	<h3><a href="https://github.com/AndrewO777/cult-game-repo">Cult</a></h3>
</div>
</template>
