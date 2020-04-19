<template>
	<div class="home-wrapper">
		<div v-bind:class="{tac: true, hide: isTacHide}">
			<div class="row">
				<div class="col-lg-10 col-md-10 col-sm-12 col-xs-12  mb-sm-3 mb-xs-3">
					By accessing and using this website, you acknowledge that you have read and understand our <a href="">Cookie Policy</a>, <a href="">Privacy Policy</a>, and our <a href="">Terms of Service</a>.
				</div>
				<div class="col-lg-2 col-md-2 col-sm-12 col-xs-12">
					<button class="btn btn-primary" v-on:click="tacHide">Got It</button>
				</div>
			</div>
		</div>
		<image-slider></image-slider>
		<div class="container-fluid">
			<div class="intro">
				<h1>How Can I Help You?</h1>
				<p>Our work then targeted, best practices outcomes social innovation synergy. Venture philanthropy, revolutionary inclusive policymaker relief. User-centered program areas scale.</p>
			</div>

			<div class="row">
				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
					  <div class="card-body">
					    <div class="card-title row">
					    	<div class="col-10">
					    		<h5>Consult</h5>
					    	</div>
					    	<div class="col-2">
					    		<span class="fa fa-comments-o"></span>
					    	</div>
				    	</div>
					    <div class="card-text">Co-create, design thinking; strengthen infrastructure resist granular. Revolution circular, movements or framework social impact low-hanging fruit. Save the world compelling revolutionary progress.</div>
					  </div>
					</div>
				</div>

				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
					  <div class="card-body">
					    <div class="card-title row">
					    	<div class="col-10">
					    		<h5>Design</h5>
					    	</div>
					    	<div class="col-2">
					    		<span class="fa fa-paint-brush"></span>
					    	</div>
				    	</div>
					    <div class="card-text">Policymaker collaborates collective impact humanitarian shared value vocabulary inspire issue outcomes agile. Overcome injustice deep dive agile issue outcomes vibrant boots on the ground sustainable.</div>
					  </div>
					</div>
				</div>

				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
					  <div class="card-body">
					    <div class="card-title row">
					    	<div class="col-10">
					    		<h5>Develop</h5>
					    	</div>
					    	<div class="col-2">
					    		<span class="fa fa-cubes"></span>
					    	</div>
				    	</div>
					    <div class="card-text">Revolutionary circular, movements a or impact framework social impact low-hanging. Save the compelling revolutionary inspire progress. Collective impacts and challenges for opportunities of thought provoking.</div>
					  </div>
					</div>
				</div>

				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
					  <div class="card-body">
					    <div class="card-title row">
					    	<div class="col-10">
					    		<h5>Marketing</h5>
					    	</div>
					    	<div class="col-2">
					    		<span class="fa fa-bullhorn"></span>
					    	</div>
				    	</div>
					    <div class="card-text">Peaceful; vibrant paradigm, collaborative cities. Shared vocabulary agile, replicable, effective altruism youth. Mobilize commitment to overcome injustice resilient, uplift social transparent effective.</div>
					  </div>
					</div>
				</div>

				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
					  <div class="card-body">
					    <div class="card-title row">
					    	<div class="col-10">
					    		<h5>Manage</h5>
					    	</div>
					    	<div class="col-2">
					    		<span class="fa fa-tasks"></span>
					    	</div>
				    	</div>
					    <div class="card-text">Change-makers innovation or shared unit of analysis. Overcome injustice outcomes strategize vibrant boots on the ground sustainable. Optimism, effective altruism invest optimism corporate social.</div>
					  </div>
					</div>
				</div>

				<div class="col-lg-4 col-md-4 col-sm-12 col-xs-12 mb-4">
					<div class="card">
					  <div class="card-body">
					    <div class="card-title row">
					    	<div class="col-10">
					    		<h5>Evolve</h5>
					    	</div>
					    	<div class="col-2">
					    		<span class="fa fa-line-chart"></span>
					    	</div>
				    	</div>
					    <div class="card-text">Activate catalyze and impact contextualize humanitarian. Unit of analysis overcome injustice storytelling altruism. Thought leadership mass  incarceration. Outcomes big data, fairness, social game-changer.</div>
					  </div>
					</div>
				</div>
			</div>
		</div>
		<div v-bind:class="{milis: true, hide: isMilisHide}">
			<div class="row">
				<div class="col-11">
					<h3>Get latest updates in web technologies</h3>
				</div>
				<div class="col-1">
					<button class="btn-hide" v-on:click="milisHide"><i class="fa fa-times"></i></button>
				</div>
			</div>
			<p>I write articles related to web technologies, such as design trends, development tools, UI/UX case studies and reviews, and more. Sign up to my newsletter to get them all.</p>
			<div class="email-input">
				<input type="text" placeholder="Email address" />
				<button>Count me in!</button>
			</div>
		</div>
	</div>
</template>

<script>
import { ImageSlider } from '../components'

export default {
	name: 'home',
	data: function() {
		return {
			isTacHide: false,
			isMilisHide: false
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

<style scoped>
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

.milis {
	position: fixed;
	background-color: #1168a6;
	color: #ffffff;
	left: 0;
	bottom: 0;
	opacity: .95;
	transition: left .5s;
}

@media all and (max-width: 768px) {
	.tac {
	  padding: 10px 10px 10px 10px;
	  font-size: 12px;
	}
	.tac.hide {
		top: -120px;
	}
	.intro {
		width: 100%;
	  margin: 60px auto 60px auto;
	  text-align: center;
	}
	.intro h1 {
		font-size: 2rem;
		font-weight: normal;
		margin-bottom: 20px;
	}
	.intro p {
		font-size: 16px;
	}
	.card {
		border-radius: 0;
		box-shadow: inset 0px 0px 1px 1px #eeeeee;
		background-color: #dddddd;
		border: 1px solid #aaaaaa;
	}
	.card .card-body .card-title h5 {
		color: #333333;
	}
	.card .card-body .card-title span {
		color: #999999;
		font-size: 24px;
	}
	.card .card-body .card-text {
		font-size: 12px;
	}	
	.milis {
		width: 100%;
		padding: 20px;
	}
	.milis.hide {
		left: -500px;
	}
	.milis h3 {
		font-size: 1.5rem;
	}
	.milis .btn-hide {
		font-size: 10px;
		color: #ffffff;
		border: 0;
		background-color: transparent;
	}
	.milis p {
		font-size: 12px;
	}
	.milis .email-input input {
		height: 24px;
		width: 100%;
		font-size: 12px;
	}
	.milis .email-input button {
		width: 100%;
		height: 24px;
		font-size: 12px;
		font-weight: bold;
		color: #ffffff;
		border: 1px solid #c49102;
		background-color: #ebad00;
	}
}

@media all and (min-width: 768px) {
	.container-fluid {
		padding-left: 30px;
		padding-right: 30px;
	}
	.tac {
	  padding: 15px 25% 10px 25%;
	  font-size: 12px;
	}
	.tac.hide {
		top: -80px;
	}
	.intro {
		width: 60%;
	  margin: 60px auto 60px auto;
	  text-align: center;
	}
	.intro h1 {
		font-weight: normal;
	}
	.intro p {
		font-size: 16px;
	}
	.card {
		border-radius: 0;
		box-shadow: inset 0px 0px 1px 1px #eeeeee;
		background-color: #dddddd;
		border: 1px solid #aaaaaa;
	}
	.card .card-body .card-title h5 {
		color: #333333;
	}
	.card .card-body .card-title span {
		color: #999999;
		font-size: 24px;
	}
	.card .card-body .card-text {
		font-size: 12px;
	}	
	.milis {
		width: 500px;
		padding: 20px;
	}
	.milis.hide {
		left: -500px;
	}
	.milis h3 {
		font-size: 1.5rem;
	}
	.milis .btn-hide {
		font-size: 10px;
		color: #ffffff;
		border: 0;
		background-color: transparent;
	}
	.milis p {
		font-size: 12px;
	}
	.milis .email-input input {
		height: 24px;
		width: 70%;
		font-size: 12px;
	}
	.milis .email-input button {
		height: 24px;
		font-size: 12px;
		font-weight: bold;
		color: #ffffff;
		border: 1px solid #c49102;
		background-color: #ebad00;
	}
}
</style>