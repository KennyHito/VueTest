<template>
	<div>
		<button @click="getStudents">获取学生信息</button>
		<button @click="getCars">获取汽车信息</button>
	</div>
</template>

<script>
import axios from 'axios'
export default {
	name: 'App',
	methods: {
		getStudents() {
			// 这里的地址根据自己本地服务器地址进行修改
			axios.get('http://localhost:8080/students').then(
				response => {
					console.log('请求成功了', response.data)
				},
				error => {
					console.log('请求失败了', error.message)
				}
			)
		},
		getCars() {
			// 这里的地址根据自己本地服务器地址进行修改
			axios.get('http://localhost:8080/demo/cars').then(
				response => {
					console.log('请求成功了', response.data)
				},
				error => {
					console.log('请求失败了', error.message)
				}
			)
		}
	},
}
</script>
