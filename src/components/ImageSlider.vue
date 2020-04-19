<template>
	<div class="image-slider-wrapper jumbotron">
		<div class="mask-layer">
			<img :src="logo" />
			<h1 class="display-4">Hello! I'm Yuan Monos</h1>
			<h3>Consult, Design, and Develop Websites</h3>
			<p>Have something great in mind? Feel free to contact me. I'll help you to make it happen.</p>
			<a class="btn btn-outline-light btn-lg" href="#" role="button">Let's Make Contact</a>			
		</div>
	</div>
</template>

<script>
import logo from '../assets/logo.png';

export default {
	name: "image-slider",
	data: function() {
		return {
			logo: logo
		}
	}
}
</script>

<style scoped>
@media all and (max-width: 768px) {
	.image-slider-wrapper {
		background-image: url(../assets/bg.jpg);
		background-size: auto 100%;
    background-position: 50%;
    height: 600px;
		border-radius: 0;
		text-align: center;
		padding: 0;
		filter: contrast(250%) brightness(90%);
	}
	.image-slider-wrapper .mask-layer {
		background-color: rgba(0, 97, 150, 0.5);
	  position: absolute;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 600px;
	  padding: 220px 20px 0 20px;
	  color: #ffffff;
	}
	.image-slider-wrapper .mask-layer img {
		position: absolute;
    width: 50px;
    height: auto;
    top: 140px;
    left: 30px;
  }
	.display-4 {
		font-size: 2rem;
		font-weight: 400;
	}
}

@media all and (min-width: 768px) {
	.image-slider-wrapper {
		background-image: url(../assets/bg.jpg);
		background-size: 100% auto;
		height: 600px;
		border-radius: 0;
		text-align: center;
		padding: 0;
		filter: contrast(250%) brightness(90%);
	}
	.image-slider-wrapper .mask-layer {
		background-color: rgba(0, 97, 150, 0.5);
	  position: absolute;
	  top: 0;
	  left: 0;
	  width: 100%;
	  height: 600px;
	  padding: 150px;
	  color: #ffffff;
	}
	.image-slider-wrapper .mask-layer img {
		position: absolute;
    width: 50px;
    height: auto;
    top: 100px;
    left: 30px;
  }
}
</style>
