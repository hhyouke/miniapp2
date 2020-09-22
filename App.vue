<script>
	export default {
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style lang="scss">
@import './style/common.scss';
page {
	height: 100%;
	background-color: #f5f5f5;
	font-size: $uni-font-size-base;
}
</style>
