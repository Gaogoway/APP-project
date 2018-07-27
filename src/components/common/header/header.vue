<template>
	<div class="box">
	<header>
		<div class="left">
			<div class="toolbar-icon" @click="isNavList=!isNavList">
				<i class="fa fa-bars"></i>
			</div>
			
			<div class="toolbar-title">
				<div class="header_tit">卖座电影</div>
			</div>
			
		</div>
		<div class="right">
			<div class="city">成都</div>
			<i class="fa fa-chevron-down"></i>
			<i class="fa fa-user-o"></i>
		</div>
	</header>
	<!--父传子这个:isNavList="isNavList"是绑定它的值就是isNavList的值-->
	<nav-list :isNavList="isNavList" @close="isNavList=flase"></nav-list>
	</div>
</template>

<script>
	import navList from "./navList.vue"
	export default{
		name:"Header",
		data(){
			return{
				isNavList:true
			}
		},
		components:{
			navList
		}
	}
</script>

<style scoped lang="scss">
	header{
		width: 320px;
		background: #282828;
		height: 50px;
		position: fixed;
		overflow: hidden;
		display: flex;
		justify-content: space-between;
		top: 0;
		
		.left{
		display: flex;
		align-items: center;
		width: 198px;
		height: 50px;
		color: #999;
		
		.toolbar-icon{
			height: 50px;
		    width: 48px;
		    line-height: 50px;
		    text-align: center;
		    border-right: 1px solid #222;
		    box-shadow: 1px 0 1px #363636;
		    color: #999;
		}
		
		.toolbar-title{
			    padding: 0 1em;
			    font-size: 14px;
			    color: #efefef;
			    text-overflow: ellipsis;
			    white-space: nowrap;
			    displdday: inline-block;
			    overflow: hidden;
		}
	}
	.right{
		display: flex;
		width: 104px;
		height: 50px;
		align-items: center;
		top: 10px;
		color: #fff;
		
		.city{
			    font-size: 14px;
   				 padding: 0 6px;
   				 color: #999;			
		}
		i{
			font-size: 12px;
			color: #999;
		}
		& i:nth-child(3){
			   
			    font-size: 16px;
			    width: 48px;
			    text-align: center;
			    color: #999;
			    font-size: 14px !important;
		}
	}
	}
	
	
</style>