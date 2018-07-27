<template>
	<div class="swiper-container banner">
    <div class="swiper-wrapper">
        <div class="swiper-slide"
        	v-for="banner in banners"
        	:key="banner.id"><img :src="banner.imageUrl" /></div>
    </div>
</div>
</template>

<script>
	import axios from "axios";
	import Swiper from "swiper";
	import "swiper/dist/css/swiper.min.css";
	export default{
		name:"banner",
		data(){
			return{
				banners:[]				
			}
		},
			methods:{
				getBanners(){
					axios.get("/static/mock/banner.json").then(res=>{
						console.log(res)
						this.banners=res.data
					})
				}
			},
			created(){
				this.getBanners()
			},
			updated(){
				new Swiper(".swiper-container",{
					loop:true,
					autoplay:true
				})
			}
	}
</script>

<style scoped lang="scss"> 
	.banner{
		position: relative;
    display: block;
    overflow: hidden;
    margin: 0;
    padding: 0;
    
    img{
    	width: 320px;
    	height: 180px;
    }
	}
</style>