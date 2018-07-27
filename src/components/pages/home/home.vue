<template>
	<div class="home">
		
		<banner></banner>
	</div>
	
	
</template>

<script>
	import banner from "./banner.vue";
	export default{
		name:"home",
		data(){
			return{
				
			}
		},
		components:{
			banner
		}
	}
</script>

<style scoped lang="scss">
	.home{
		margin-top: 50px;
	}
</style>