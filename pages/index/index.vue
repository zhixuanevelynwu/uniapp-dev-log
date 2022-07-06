<template>
	<!-- v-bind OR 	: 	represents dynamic class name -->
	<!-- v-on 	OR	@	represents events -->
	<view class="content" :class="className" @click="open">
		{{title}}
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: "hello world :O",
				className: "active"
			}
		},
		onLoad() {
			setTimeout(()=>{
				/*	original way:
					this.setData({
						title: "hello uni-app"
					})
				*/
				// this.title = "hello uni-app"
			}, 2000)
		},
		methods: {
			// custom methods go here
			open() {
				console.log("clicked");
				this.title = "I'm clicked..."
			}
		}
	}
</script>

<style>
</style>
