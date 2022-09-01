<template>
	 <view>
		 <!-- #ifdef H5 -->
		 <view>
			这是H5界面展示的东西
		 </view>>
		 <!-- #endif -->
		 <!-- #ifdef MP-WEIXIN -->
		 <view>
			 这是微信小程序界面展示的东西
		 </view>
		 <!-- #endif -->
		 <button @click="test" type="primary">test</button>
	 </view>
	
</template>

<script>
	export default{
		data(){
			return{
				
			}
		},
		methods:{
			test(e){
				console.log(e);
				// #ifdef H5
				console.log("这是H5界面专门的输出");
				// #endif
				// #ifdef MP-WEIXIN
				console.log("这是微信小程序的界面");
				// #endif
			}
		}
	}
</script>

<style>
</style>