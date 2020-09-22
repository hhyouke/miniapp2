<template>
	<view class="wrapper">
		<!-- course block -->
		<view class="course-block">
			<view class="course-header">
				<text>course</text>
				<text v-show="courses.length > 1">more</text>
			</view>
			<view class="course-list">
				<view v-for="(item, index) in courses" :key="item.course_id" @click="onOpenCourse(item)">
					<view class="title">{{ item.title }}</view>
				</view>
			</view>
		</view>
		<!-- classroom block -->
		<view class="classroom-block">
			<view class="classroom-header">
				<text>classrooms</text>
				<text v-show="courses.length > 1">more</text>
			</view>
			<view class="classroom-list">
				<view v-for="(item, index) in classrooms" :key="item.id" @click="onOpenClass(item)">
					<view class="name">{{ item.name }}</view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
	// import swipeAction from '@/components/common/swipe-action/index.vue';
	export default {
		components: {
		},
		data() {
			return {
				courses: [{
					course_id: 5641,
					title: 'test-cc',
					desc: 'cc for test',
					sections: 3,
					lessons: 18,
					author: 'admin',
					progress: 0.6
				},{
					course_id: 5642,
					title: 'test-cc2',
					desc: 'cc for test',
					sections: 3,
					lessons: 18,
					author: 'admin',
					progress: 0.6
				}], 
				classrooms: [{
					class_id: 432,
					name: 'test-cls',
					members: 46,
				}],
			}
		},
		onLoad() {
			// fetch recent visited courses and classrooms
		},
		methods: {
			onOpenCourse(item) {
				uni.navigateTo({
					url: "/pages/course/detail?courseId=" + item.course_id
				})
			},
			onOpenClass(item) {
				uni.navigateTo({
					url: "/pages/classroom/goodsDetail?id=" + item.class_id
				})
			},
		}
	}
</script>

<style>
	
</style>
