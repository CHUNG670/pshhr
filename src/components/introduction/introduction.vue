<template>
	<div class="background">
		<div class="introduction">
			<div class="left">
				<p>{{title}}</p>
				<p>{{englishtitle}}</p>
			</div>
			<div class="right">
				<transition name="top">
					<div v-show="show">
						<p class="p1" v-for="(p,index) in p1">{{p}}</p>
					</div>
				</transition>
				<transition name="fade">
					<div class="line" v-show="show"></div>
				</transition>
				<transition name="top">
					<div v-show="show">
						<p class="p2" v-for="(p,index) in p2">{{p}}</p>
					</div>
				</transition>
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		props:{
			title: {
				type: String,
				default: '中文标题'
			},
			englishtitle: {
				type: String,
				default: '英文标题'
			},
			p1: {
				type: Array,
				default: ['中文简介']
			},
			p2: {
				type: Array,
				default: ['英文简介']
			},
		},
		data() {
			return {
				show: false
			}
		},
		mounted(){
			setTimeout(()=>{
				this.show = true
			},500)
		}
	}
</script>

<style lang="scss" scoped>
	.background {
		width: 100%;
		background: #0e132d;
	}

	.introduction {
		color: #fff;
		display: flex;
		justify-content: space-between;
		width: 1200px;
		margin: 0 auto;
		padding: 150px 0;

		.left {
			p {
				font-size: 50px;
				line-height: 60px;
				font-weight: normal;
			}
		}

		.right {
			margin-left: 150px;

			p {
				font-size: 14px;
				line-height: 28px;
				margin-bottom: 20px;
			}

			.line {
				width: 320px;
				border-top: 1px solid #ffffff;
				margin: 40px 0;
			}
		}

	}
</style>
