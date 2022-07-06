<template>
	<!-- template can only contain 1 direct child element -->
	<!-- if -->
	<view>
		<view v-if="show === 'uni-app'">hello world 0</view>
		<view>hello world 1</view>
		<view>{{show ? "show == true" : "show == false"}}</view>
		
		<view>
			<view v-if="show">element 0</view>
			<!-- <view v-else-if="show">element 0.5</view> -->
			<view v-else>element 1</view>
		</view>
		
		<button type="default" @click="open">click me</button>
	</view>
	
</template>

<script>
	export default {
		data() {
			return {
				show: false
			}
		},
		onLoad() {
		},
		methods: {
			open() {
				this.show = !this.show
			}
		}
	}
</script>

<style>
</style>
