<template>
	<view>
		<view class="title">{{ courseInfo.title }}</view>
		<!-- sections -->
		<view v-for="(section, index) in courseInfo.sections" :key="section.section_id">
			<view class="title">{{ section.title }}</view>
			<!-- lessons -->
			<view v-for="(lesson, index) in section.lessons" :key="lesson.lesson_id" @click="onOpenLesson(lesson)">
				<button @click="onEditLesson(lesson)">edit</button>
				<view class="title">{{ lesson.title }}</view>
			</view>
		</view>
	</view>
</template>

<script>
	export default {
		props: {
			courseId: ''
		},
		data() {
			return {
				courseInfo: {
					banner: '',
					title: '',
					author: '',
					sections: [{
						section_id: 'sec1',
						title: 'test-section',
						desc: 'test-section',
						lessons: [{
							lesson_id: 'les1',
							title: 'les1',
							content_type: 1000,
							content_src: '<div style="text-align:center;"><img src="https://img-cdn-qiniu.dcloud.net.cn/uniapp/images/uni@2x.png"/></div>',
							gist: 'lalala'
						}]
					}]
				}
			}
		},
		methods: {
			onOpenLesson(lesson){
				uni.navigateTo({
					url: "/pages/lesson/index?lessonId=" + lesson.lesson_id + "&contentType=" + lesson.content_type
				})
			},
			onEditLesson(lesson){
				uni.navigateTo({
					url: "/pages/lesson/edit?contentSrc="+encodeURIComponent(JSON.stringify(lesson.content_src))+"&contentType="+lesson.content_type
				})
			},
		}
	}
</script>

<style>

</style>
