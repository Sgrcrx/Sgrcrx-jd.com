<template>
	<div class="search">
		<ul>
			<li v-for="(item,index) in productes" v-text="item.title"></li>
		</ul>
		<footeres></footeres>
	</div>
</template>

<script>
	//axios
	import axios from 'axios'
	import Footeres from '../components/Footeres'

	export default {
		data(){
			return{
				productes: []
			}
		},
		
		name: 'search',
		components: {
			Footeres
		},
		mounted() {
			axios.get("/data.json").then(res => {
				this.productes = res.data;
			}).catch(err => {

			});
		}
	}
</script>

<style>

</style>