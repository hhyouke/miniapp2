<template>
	<view>
		<view class="title">{{ id }}</view>
		<view class="title">{{ type }}</view>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				id:'',
				type: '',
			}
		},
		onLoad(option) {
			console.log(option)
			this.id = option.lessonId
			this.type = option.contentType
		},
		methods: {
			
		}
	}
</script>

<style>

</style>
