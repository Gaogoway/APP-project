<template>
	<div class="nav-list page">
		<transition
			enter-active-class="animated fadeIn"
			leave-active-class="animated fadeOut">
			<!--遮罩-->
			<div class="mask" @click="$emit('close')" v-if="isNavList">
				
			</div>
			</transition>
		
		<transition
			enter-active-class="animated slideInLeft"
			leave-active-class="animated slideOutLeft">
		<ul v-if="isNavList">
			<li
				v-for="nav in navs"
				:key="nav.id"
				>
				{{nav.title}}
				<i class="fa fa-angle-right"></i>
			</li>
		</ul>
		</transition>
		
		
	</div>
</template>

<script>
	export default{
		name:"navList",
		props:["isNavList"],
		data(){
			return{
				navs:[
					{id:1,title:"首页"},
					{id:2,title:"影片"},
					{id:3,title:"影院"},
					{id:4,title:"商城"},
					{id:5,title:"我的"},
					{id:6,title:"卖座卡"}
				]
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
		z-index: 4;
		
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
		z-index: 3;
		top: 50px;
		
	}
</style>