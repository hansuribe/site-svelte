<script>
	import Social from "../components/Social.svelte"
</script>
<style>
#hello {
	display: grid;
	width: 100%;
	height: 100vh;
	overflow: hidden;
	min-height: 735px;
	align-content: center;
	justify-content: center;
	background-position: fixed;
	background-size: cover;
	position: fixed;
	top: 0;
	left: 0;
	z-index: 400
}
.overlay {
	position: fixed;
	top: 0;
	left: 0;
	width: 100vw;
	height: 100vh;
	background-color: rgba(0 0 0 / 40%);
	z-index:1
}
#itsMe {
	position: relative;
	z-index: 100;
	max-width: 480px;
	width: 80%
}
#itsMe picture,
#itsMe img {
	width: 200px;
	height: 200px
}
#itsMe img {
	border-radius: 50%;
	border: 5px solid rgba(255 255 255 / 80%)
}
#itsMe picture { margin-bottom: 1.5rem }
#itsMe h1 {
	font-size: clamp(2.2rem,2.6rem,10vw);
	margin-bottom: 10px
}
#itsMe p { font-size: 1.2rem }
@media screen and (max-width:450px){
	#hello { background-image: url("/images/railway-360.jpg") }
}
@media screen and (min-width:450px) and (max-width:768px){
	#hello { background-image: url("/images/railway-768.jpg") }
}
@media screen and (max-width:750px){
	#itsMe { padding-top: 3rem }
}
@media screen and (min-width:768px) and (max-width:1440px){
	#hello { background-image: url("/images/railway-1440.jpg") }
}
@media screen and (min-width:1440px){
	#hello { background-image: url("/images/railway-2048.jpg") }
}
@media screen and (max-width:420px){
	footer#front { max-width: 260px }	
}
</style>

<div id="hello" class="tc obj">
	<div class="overlay"></div>
	<div id="itsMe" class="mxa">
		<picture id="pic" class="mxa">
			<source srcset="/images/timo.webp" type="image/webp">
			<source srcset="/images/timo.jpg" type="image/jpeg">
			<img src="/images/timo.jpg" alt="Timo Anttila">
		</picture>
		<h1>Timo Anttila</h1>
		<p>Full Stack Web Developer, photographer and sea adventurer from Nokia, Finland. Making websites for a living and amuse people as a hobby.</p>
	</div>
	<footer id="front" class="mxa"><Social/></footer>
</div>
