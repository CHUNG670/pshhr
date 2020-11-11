<template>
	<div class="about">
		<div class="video-div">
			<heada></heada>
			<video class="video" muted autoplay loop>
				<source src="../static/video/about.mp4" type="video/mp4">
				</source>
			</video>
			<div class="title">
				<p class="p">RONG HE</p>
				<p class="p1">为企业智慧经营全面赋能的营销科技公司</p>
				<p class="p2">A marketing technology company dedicated to enhancing our clients’ enterprise capabilities through
					intelligent management and operation</p>
			</div>
		</div>
		<div class="introduction">
			
		</div>
	</div>
</template>

<script>
	import heada from '../components/header/index.vue'
	export default {
		components: {
			heada
		}
	}
</script>

<style lang="scss" scoped>
	//.about{}
	.video-div {
		position: relative;
		height: calc(100vh);
		width: 100%;
		overflow: hidden;
		z-index: -2;

		.video {
			position: absolute;
			top: 0;
			left: 0;
			z-index: -1;
			min-height: 100%;
			min-width: 100%;
			height: auto;
			width: auto;
			background: url(../static/img/homepage.jpg) no-repeat;
			background-size: cover;
		}

		.title {
			position: absolute;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
			color: #FFFFFF;
			text-align: center;
			
			.p{
				font-size: 100px;
			}

			.p1 {
				margin-top: 40px;
				font-size: 18px;
				letter-spacing: 5px;
			}

			.p2 {
				font-size: 16px;
				margin: 10px auto 0;
			}
		}
	}

	.introduction{
		background: #0e132d;
		color: #fff;
		display: flex;
		margin: 0 auto;
		padding: 150px 0;
	}
</style>
