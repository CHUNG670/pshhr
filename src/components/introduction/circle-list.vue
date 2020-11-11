<template>
	<div class="circle-list">
		<div class="circle" v-for="(item,index) in showlist" :key='index'>
			<p><span>{{item.num}}</span>{{item.unit}}</p>
			<p>{{item.title}}</p>
			<p>{{item.english}}</p>
		</div>
	</div>
</template>

<script>
	export default {
		data(){
			return {
				showlist: [{
					num: 281,
					unit: '元',
					title: '年度总营收',
					english: 'Annual Revenue'
				}]
			}
		}
	}
</script>

<style lang="scss" scoped>
	.circle-list{
		background: #0e132d;
		display: flex;
		justify-content: center;
		margin-top: -120px;
		padding-bottom: 150px;
		
		.circle{
			border: 1px solid #b1b1b1;
			border-radius: 50%;
			margin-left: 33px;
			width: 170px;
			height: 170px;
			
			p{
				width: 100%;
				text-align: center;
				font-size: 12px;
				color: #b1b1b1;
				
				span{
					font-size: 60px;
				}
			}
			
			p:first-child {
			    color: #fff;
			    margin-top: 36px;
			}
		}
	}
	
</style>
