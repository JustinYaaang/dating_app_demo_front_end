<template>
    <view class="container">
        HelloWorld, ChongBao
		<image src="../../static/grid/banner1.png"></image>
		<!-- <Ytitle value='这是带数字标题' pieceColor='#007AFF' num='333'></Ytitle> -->
		<!-- <YinfoList :config="config" :data="data"></YinfoList> -->
    </view>
</template>

// <script>
// 	export default {
// 		data() {
// 			return {
// 				mark: 0
// 			}
// 		},
// 		methods: {
// 			addMark () {
// 				//通过this.调用data对象中定义的变量
// 				console.log("mark变量为：", this.mark)
// 			}
// 		},
// 		mounted() {
// 			this.addMark()
// 		}
// 	}
// </script>

// <script>
	export default {

	data() {
		return {
	        config: [
				{
					title: '用户名',
					key: 'username'
	            },
				{
					title: '性别',
					key: 'sex'
				},
				{
					title: '手机号',
					key: 'phone'
				},
				{
					title:'地址',
					key:'address'
				},
				{
					title:'出生日期',
					key:'birthday'
				},
	        ],
			data: {
					username: '李大锤',
					sex: '男',
					phone: '15095111111',
					address: '北京前门外前门大街',
					birthday: '2000-10-01'
	        }
		}
	}
	}
//</script>>


<style>
	.container {
		padding: 20px;
		font-size: 14px;
		line-height: 24px;
	}
</style>
