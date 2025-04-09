<template>
	<div class="col-xs-offset-2 col-xs-8">
		<div class="page-header">
			<h2>Vue Router Demo</h2>
			<button @click="saveSchool">存储学校</button>
			<button @click="removeSchool">移除学校</button>
			<button @click="back">后退</button>
			<button @click="forward">前进</button>
			<button @click="test">测试一下go</button>
		</div>
	</div>
</template>

<script>
	export default {
		name:'Banner',
		methods: {
			back(){
				this.$router.back()
				// console.log(this.$router)
			},
			forward(){
				this.$router.forward()
			},
			test(){
				this.$router.go(3)
			},
			saveSchool(){
				window.localStorage.setItem('school','atguigu')
			},
			removeSchool(){
				window.localStorage.removeItem('school')
			}
		},
	}
</script>