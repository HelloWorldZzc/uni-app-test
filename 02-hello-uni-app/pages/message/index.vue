<template>
	<view class="content">
		<input placeholder="第一个数" v-model="data1"/>
		<view>
			-----------------------------------
		</view>
		<input placeholder="第二个数" v-model="data2"/>
		<button @click="test ">battle</button>
	</view>
</template>

<script>
	export default{
		data(){
			return{
				data1:" ",
				data2:" "
			}
		},
		methods: {
			test(){
				this.data1>this.data2?wx.showToast({
					title:"第一个数大"
				}):wx.showToast({
					title:"第二个数大"
				})
			}
		}
	}
</script>

<style>
	input{
		background-color: bisque;
	}
</style>