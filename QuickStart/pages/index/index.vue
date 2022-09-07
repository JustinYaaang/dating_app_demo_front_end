<template>
    <view class="container">
        HelloWorld, ChongBao
    </view>
</template>

<script>
	export default {
		data() {
			return {
				mark: 0
			}
		},
		methods: {
			addMark () {
				//通过this.调用data对象中定义的变量
				console.log("mark变量为：", this.mark)
			}
		},
		mounted() {
			this.addMark()
		}
	}
</script>


<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
