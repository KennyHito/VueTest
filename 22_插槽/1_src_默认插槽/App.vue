<template>
	<div class="container">
		<Category title="美食">
			<img src="https://s3.ax1x.com/2021/01/16/srJlq0.jpg" alt="">
		</Category>

		<Category title="游戏">
			<ul>
				<li v-for="(g, index) in games" :key="index">{{ g }}</li>
			</ul>
		</Category>

		<Category title="电影">
			<video controls
				src="https://upos-sz-mirrorcos.bilivideo.com/upgcxcode/17/99/1034909917/1034909917-1-16.mp4?e=ig8euxZM2rNcNbRVhwdVhwdlhWdVhwdVhoNvNC8BqJIzNbfq9rVEuxTEnE8L5F6VnEsSTx0vkX8fqJeYTj_lta53NCM=&uipk=5&nbs=1&deadline=1742196877&gen=playurlv2&os=bcache&oi=2032490763&trid=000073654da7d4c242008eb1f4b3d65bf736h&mid=0&platform=html5&og=cos&upsig=6299d51493587c585af6b4d1a7af8714&uparams=e,uipk,nbs,deadline,gen,os,oi,trid,mid,platform,og&cdnid=71508&bvc=vod&nettype=0&f=h_0_0&bw=9858&logo=80000000"></video>
		</Category>
	</div>
</template>

<script>
import Category from './components/Category'
export default {
	name: 'App',
	components: { Category },
	data() {
		return {
			foods: ['火锅', '烧烤', '小龙虾', '牛排'],
			games: ['红色警戒', '穿越火线', '劲舞团', '超级玛丽'],
			films: ['《教父》', '《拆弹专家》', '《你好，李焕英》', '《尚硅谷》']
		}
	},
}
</script>

<style scoped>
.container {
	display: flex;
	justify-content: space-around;
}
</style>
