<template>
	<view class="content">
		<!-- courses -->
		<uni-list>
			<uni-list-item v-for="" :key="" title=""></uni-list-item>
		</uni-list>
		<!-- classes -->
		<uni-list>
			<uni-list-item v-for="" :key="" title=""></uni-list-item>
		</uni-list>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				myCourses: [], // my-courses-visited-desc
				myClasses: [], // my-classes-visited-desc
			}
		},
		onLoad() {
			// fetch my courses and classes
		},
		methods: {

		}
	}
</script>

<style>
	
</style>
