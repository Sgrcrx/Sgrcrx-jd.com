<template>
	<div class="ceshi">
		<swipera></swipera>
	</div>
</template>

<script>
	import Swipera from '../components/Swipera'
	import axios from "axios"
	export default {
		data() {
			return {
				product: []
			};
		},
		components: {
			Swipera
		},
		created() {
			// 当前页面的路由对象
			console.log(this.$route);
			console.log(this.$router);
		}
	}
</script>

<style scoped="scoped">
		
</style>