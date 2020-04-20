<template>
	<div class="home-wrapper">
		<div v-bind:class="{tac: true, hide: isTacHide}">
			<div class="row">
				<div class="col-lg-10 col-md-10 col-sm-12 col-xs-12  mb-sm-3 mb-xs-3">
					Dengan mengakses dan menggunakan situs web ini, Anda mengetahui bahwa Anda telah membaca dan memahami <a href="">Kebijakan Cookie</a>, <a href="">Kebijakan Privacy</a>, dan <a href="">Ketentuan Layanan</a> kami.
				</div>
				<div class="col-lg-2 col-md-2 col-sm-12 col-xs-12">
					<button class="btn btn-primary" v-on:click="tacHide">Setuju</button>
				</div>
			</div>
		</div>
		<image-slider></image-slider>
		<div class="container-fluid">
			<div class="intro">
				<h1>Work From Home dan Laper?</h1>
				<p>Silakan pesan makanan dari menu-menu yang tersedia berikut ini.</p>
			</div>

			<div class="row">

				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
						<div class="card-body">
							<div class="card-title">
								<h5>Ayam Srundeng</h5>
							</div>
							<div class="card-img">
								<img :src="ayamSrundeng" />
							</div>
							<div class="card-text">
								<p>Ayam goreng dengan taburan srundeng.</p>
								<p class="price">Rp. 45.000 / pack</p>
							</div>
						</div>
					</div>
				</div>

				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
						<div class="card-body">
							<div class="card-title">
								<h5>Omelet Basil</h5>
							</div>
							<div class="card-img">
								<img :src="omeletBasil" />
							</div>
							<div class="card-text">
								<p>Telur dadar dengan campuran sayuran basil.</p>
								<p class="price">Rp. 25.000 / pack</p>
							</div>
						</div>
					</div>
				</div>

				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
						<div class="card-body">
							<div class="card-title">
								<h5>Ayam Semur</h5>
							</div>
							<div class="card-img">
								<img :src="ayamSemur" />
							</div>
							<div class="card-text">
								<p>Ayam dimasak semur dengan rasa manis dan gurih.</p>
								<p class="price">Rp. 45.000 / pack</p>
							</div>
						</div>
					</div>
				</div>

			</div>
		</div>
	</div>
</template>

<script>
import { ImageSlider } from '../components'
import ayamSrundeng from '../assets/ayam-srundeng.jpg';
import omeletBasil from '../assets/omelet-basil.jpg';
import ayamSemur from '../assets/ayam-semur.jpg';

export default {
	name: 'home',
	data: function() {
		return {
			isTacHide: false,
			isMilisHide: false,
			ayamSrundeng: ayamSrundeng,
			omeletBasil: omeletBasil,
			ayamSemur: ayamSemur
		}
	},
	components: {
		ImageSlider
	},
	methods: {
		tacHide() {
			this.isTacHide = true
		},
		milisHide() {
			this.isMilisHide = true
		}
	}
}
</script>

<style lang="scss" scoped>
.home-wrapper {
	background-color: #dddddd;
}
.tac {
		background-color: #cccccc;
		position: fixed;
		z-index: 999;
		top: 0px;
		transition: top .5s;
}

@media all and (max-width: 768px) {
	.tac {
		padding: 10px 10px 10px 10px;
		font-size: 12px;

		&.hide {
			top: -120px;
		}
	}

	.intro {
		width: 100%;
		margin: 20px auto 30px auto;
		text-align: center;

		h1 {
			font-size: 2rem;
			font-weight: normal;
			margin-bottom: 20px;
		}

		p {
			font-size: 16px;
		}
	}

	.card {
		border-radius: 0;
		box-shadow: inset 0px 0px 1px 1px #eeeeee;
		background-color: #dddddd;
		border: 1px solid #aaaaaa;

		.card-body {
			.card-title {
				h5 {
					color: #333333;
				}
			}

			.card-img {
				margin-bottom: 20px;

				img {
					width: 100%;
					height: 200px;
					object-fit: cover;
					padding: 5px;
					border: 1px solid #cccccc;
					background-color: #e3e3e3;
				}
			}

			.card-text {
				p {
					font-size: 16px;

					&.price {
						color: #ff9900;
						font-size: 16px;
						font-weight: bold;
						margin-bottom: 0;
					}

				 	span {
						color: #ff0000;
						text-align: right;
					}
				}
			}	
		}
	}
}

@media all and (min-width: 768px) {
	.container-fluid {
		padding-left: 30px;
		padding-right: 30px;
	}

	.tac {
		padding: 15px 15% 0px 15%;
		font-size: 12px;

		&.hide {
			top: -80px;
		}
	}

	.intro {
		width: 60%;
		margin: 30px auto 40px auto;
		text-align: center;

		h1 {
			font-weight: normal;
		}

		p {
			font-size: 16px;
		}
	}

	.card {
		border-radius: 0;
		box-shadow: inset 0px 0px 1px 1px #eeeeee;
		background-color: #dddddd;
		border: 1px solid #aaaaaa;

		.card-body {
			.card-title {
				h5 {
					color: #333333;
				}
			}

			.card-img {
				margin-bottom: 20px;

				img {
					width: 100%;
					height: 200px;
					object-fit: cover;
					padding: 5px;
					border: 1px solid #cccccc;
					background-color: #e3e3e3;
				}
			}

			.card-text {
				p {
					font-size: 16px;

					&.price {
						color: #ff9900;
						font-size: 16px;
						font-weight: bold;
						margin-bottom: 0;
					}

				 	span {
						color: #ff0000;
						text-align: right;
					}
				}
			}
		}
	}
}
</style>