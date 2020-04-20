<template>
	<div class="image-slider-wrapper jumbotron">
		<div class="mask-layer">
			<img :src="logo" />
			<h1 class="display-4">Hi, kami Dapur Hafi ...</h1>
			<h3>Silakan memesan dari menu-menu yang tersedia.</h3>
			<p>Untuk saat ini area layanan kami untuk wilayah Yogyakarta. Pemesanan dapat dilakukan melalui Whatsapp / Telfon / SMS ke 081392274497.</p>
			<a class="btn btn-outline-light btn-lg" href="https://api.whatsapp.com/send?phone=6281392274497&text=Hi, Dapur Hafi ..." role="button">Pesan Sekarang</a>			
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

<style lang="scss" scoped>
@media all and (max-width: 768px) {
	.image-slider-wrapper {
		position: relative;
		width: 100%;
		height: 600px;
		border-radius: 0;
		text-align: center;
		padding: 0;

		&:before {
			content: "";
			position: absolute;
			left: 0;
			top: 0;
			background-image: url(../assets/bg.jpg);
			background-size: auto 100%;
	    background-position: 50%;
	    width: 100%;
	    height: 600px;
			border-radius: 0;
			text-align: center;
			padding: 0;
			filter: contrast(100%) brightness(50%);
		}

		.mask-layer {
		  position: absolute;
		  top: 0;
		  left: 0;
		  width: 100%;
		  height: 600px;
		  padding: 220px 20px 0 20px;
		  color: #ffffff;

		  img {
				position: absolute;
		    width: 80px;
		    height: auto;
		    top: 100px;
		    left: auto;
		    margin-left: -40px;
  		}
		}
	}

	.display-4 {
		font-size: 2rem;
		font-weight: 400;
	}
}

@media all and (min-width: 768px) {
	.image-slider-wrapper {
		position: relative;
		width: 100%;
		height: 600px;
		border-radius: 0;
		text-align: center;
		padding: 0;

		&::before {
			content: "";
			position: absolute;
			left: 0;
			top: 0;
			width: 100%;
			height: 600px;
			background-image: url(../assets/bg.jpg);			
			background-size: 100% auto;
			filter: contrast(100%) brightness(50%);
		}

		.mask-layer {
		  position: absolute;
		  top: 0;
		  left: 0;
		  width: 100%;
		  height: 600px;
		  padding: 230px 20% 0 20%;
		  color: #ffffff;

		  img {
				position: absolute;
		    width: 80px;
		    height: auto;
		    top: 100px;
		    left: 30px;
		    border-radius: 50%;
		  }

		  p {
		  	font-size: 20px;
		  }
		}
	}
}
</style>
