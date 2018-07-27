<template>
	<div class="nav-list page">
		
		<!--遮罩-->
		<div class="mask" @click="$emit('close')" v-if="isNavList">
			
		</div>
		
		<ul v-if="isNavList">
			<li>
				首页
				<i class="fa fa-angle-right"></i>
			</li>
			<li>
				影片
				<i class="fa fa-angle-right"></i>
			</li>
			<li>
				影院
			<i class="fa fa-angle-right"></i>
			</li>
			<li>				
				商城
			<i class="fa fa-angle-right"></i>
			</li>
			<li>				
				我的
			<i class="fa fa-angle-right"></i>
			</li>
			<li>			
				卖座卡
			<i class="fa fa-angle-right"></i>
			</li>
		</ul>
		
		
	</div>
</template>

<script>
	export default{
		name:"navList",
		props:["isNavList"],
		data(){
			return{
				
			}
		}
	}
</script>

<style scoped lang="scss">
	ul{
		width: 210px;
		height: 670px;
		background: #282828;
		color: #999;
		position: absolute;
		
		li{
			width: 210px;
			height: 50px;
			line-height: 50px;
			display: flex;
			justify-content: space-between;
			align-items: center;
			padding:0 16px;
		}
	}
	.mask{
		width: 320px;
		height: 670px;
		background: rgba(0,0,0,0.5);
		position: absolute;
		top: 50px;
		z-index: -1;
	}
</style>