<template>
	<view>
		<myeditor class="editor" 
		    @cancel="hideEditor" 
		    @save="saveEditor" 
		    :html="contentSrc"
		    :imageUploader="uploadImg" 
		    :muiltImage="true">
		</myeditor>
	</view>
</template>

<script>
	import myeditor from "@/components/common/editor/editor.vue"
	export default {
		components: {myeditor},
		data() {
			return {
				id: '',
				contentType: '',
				contentSrc: ''
			}
		},
		onLoad(option) {
			this.id = option.lessonId
			this.contentType = option.contentType
			this.contentSrc = JSON.parse(decodeURIComponent(option.contentSrc))
			// if (this.contentType === '1000') {
			// 	uni.navigateTo({
			// 		url: '/pages/component/editor/editor?contents='+option.contentSrc
			// 	})
			// }
			// if(this.contentSrc) {
			// 	let a = uni.createSelectorQuery().select('#ed1')
			// 	console.log(a)
			// }
		},
		methods: {

		}
	}
</script>

<style>

</style>
