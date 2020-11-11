<template>
	<div class="about">
		<div class="video-div">
			<heada></heada>
			<video class="video" muted autoplay loop>
				<source src="../static/video/about.mp4" type="video/mp4">
				</source>
			</video>
			<div class="text">
				<transition name="fade">
					<p class="p" v-show="show">RONG HE</p>
				</transition>
				<transition name="top">
					<p class="p1" v-show="show">为企业智慧经营全面赋能的营销科技公司</p>
				</transition>
				<transition name="top">
					<p class="p2" v-show="show">A marketing technology company dedicated to enhancing our clients’ enterprise
						capabilities through
						intelligent management and operation</p>
				</transition>
			</div>
		</div>
		<introduction :title="title" :englishtitle="englishtitle" :p1="p1" :p2="p2"></introduction>
		<circle-list></circle-list>
	</div>
</template>

<script>
	import heada from '../components/header/index.vue'
	import introduction from '../components/introduction/introduction.vue'
	import circleList from '../components/introduction/circle-list.vue'
	export default {
		components: {
			heada,
			introduction,
			circleList
		},
		data() {
			return {
				show: false,
				title: '公司介绍',
				englishtitle: 'INTRODUCTION',
				p1: [
					'蓝色光标是一家在大数据和社交网络时代为企业智慧经营全面赋能的营销科技公司。蓝色光标及其旗下子公司的业务板块有营销服务（数字营销、公共关系、活动管理等）、数字广告（移动广告、智能电视广告、中国企业出海数字广告）和国际及港澳台地区业务，服务内容涵盖营销传播整个产业链，以及基于数据科技的智慧经营服务，服务地域基本覆盖全球主要市场。',
					'蓝色光标业务的历史最早可以追溯至1996年。 蓝色光标于2010年在深圳证券交易所创业板上市（ 股票代码： 300058）， 2019 年公司营业收入超过281亿人民币。 公司总部位于北京， 现有员工近5,000 人， 在中国各大区域设有分支机构， 并在北美、 欧洲以及亚太其他国家和地区拥有国际业务网络。',
					'蓝色光标持续服务于约3,000 个国内外品牌客户， 其中财富500强企业100多个。 客户涵盖游戏、 汽车、 互联网及应用、 电子商务、 高科技产品、 消费品、 房地产以及金融八大行业的知名品牌。',
					'蓝色光标位列北京民营企业百强第17名， 北京民营企业文化产业百强第5名，《 财富》 中国500强第365位， 中国民营企业500强第373位， 是首都文化企业30强单位、 北京文化产业投融资协会联席会长单位、 首都文化产业协会常务理事单位、 中国广告协会副会长单位、 中国4A协会副理事长单位。 蓝色光标不断探索营销新技术新方法， 累计拥有超百项技术专利及软件著作权， 并发布了智能自动化人机交互产品族“ 小蓝机器人家族”， 推动和引领行业变革， 被北京市科委认定为“ 众创空间” 和“ 北京市设计创新中心”。'
				],
				p2: [
					'BlueFocus is a marketing technology company dedicated to enhancing our clients’ enterprise capabilities through intelligent management and operation in the era of big data and social networks. Major service offerings provided by BlueFocus and its subsidiaries are marketing services (public relations, digital marketing, event management), digital advertising (digital media placement for mobile, smart TV and other channels outside China) and international business. With a global network, our expertise covers a broad range of services in marketing communications as well as intelligent management and operation based on data technology.',
					'BlueFocus was listed on the Shenzhen Stock Exchange/Growth Enterprise Market (300058.SZ) in 2010 and its history dates back to 1996. BlueFocus employs around 5,000 talents worldwide and its revenues reached RMB 28.1 billion in 2019. Headquartered in Beijing, BlueFocus has regional branch offices in mainland China, as well as a global network in North America, Europe and Asia-Pacific region.',
					'BlueFocus provides services to over 3,000 clients, both international and Chinese companies in the online game industries, automobile, Internet, E-commerce, high-tech, consumer goods, real estate, finance, around 100 of them are Fortune 500 companies.',
					'BlueFocus is selected as one of the top 30 cultural enterprises in Beijing and holds several positions in cultural industry related associations in Beijing and members of major advertising associations in China. In the meantime, BlueFocus is the holder of over 70 software copyrights and about 20 technology patents.'
				],
			}
		},
		mounted() {
			setTimeout(() => {
				this.show = true
			}, 500)
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

		.text {
			position: absolute;
			top: 50%;
			left: 50%;
			transform: translate(-50%, -50%);
			color: #FFFFFF;
			text-align: center;

			.p {
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
</style>
