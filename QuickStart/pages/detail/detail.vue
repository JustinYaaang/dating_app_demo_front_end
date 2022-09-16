<style>
@import "../../style/fonts/icon1/iconfont.css";
</style>

<template>
	<view>
		<!-- 页面顶部导航栏 -->
		<view class="user-like-info">
			<view class="like-photo">				
				<view class="cover-image-item">
					<image :src=personInfo.pic[0]>
						<view class="user-name">达达信徒 27</view>
						<view class="user-job">无业游民</view>
						<view class="user-school">克莱登大学</view>
						
					</image>
					
				</view>																								
			</view>		
				
			<view class="text-mode">
				<view class="title-mode">关于我...</view>
				<view class="basic-info">
					<view class="basic-info-mode">162cm</view>
					<view class="basic-info-mode">天蝎座</view>
					<view class="basic-info-mode">家乡·四川 成都</view>
					<view class="basic-info-mode">目的·脱单/交朋友/拓展人脉</view>					
				</view>
			</view>		
																						
			<view class="text-mode">
				<view class="title-mode">我的日常...</view>
				<view class="normal-line-list">					
					<view class="normal-line">· 没有耳机<view class="iconfont icon-pinglun"></view>不能活星人</view>
					<view class="normal-line">· 公司和家两点一线的生活</view>
					<view class="normal-line">· 读书音乐篮球</view>					
				</view>				
			</view>

			<view class="text-mode">
				<view class="title-mode">我的愿望...</view>
				<view class="normal-line-list">
					<view class="normal-line">· 疫情早日结束</view>
					<view class="normal-line">· 多伦多的冬,雪下得温柔些</view>
					<view class="normal-line">· 每个人都被善待</view>					
				</view>				
			</view>
			
			<view class="like-photo">
				<view class="normal-image-item"><image :src=personInfo.pic[1]></image></view>																								
			</view>	
			
			<view class="text-mode">
				<view class="title-mode">我喜欢的音乐...</view>
				<view class="normal-line-list">
					<view class="normal-line">· HipHop</view>
					<view class="normal-line">· Jazz</view>
				</view>				
			</view>
			
			<view class="text-mode">
				<view class="title-mode">我喜欢的电影...</view>
				<view class="normal-line-list">
					<view class="normal-line">· 杨德昌</view>
					<view class="normal-line">· 北野武</view>
				</view>				
			</view>
			
			<view class="like-photo">
				<view class="normal-image-item"><image :src=personInfo.pic[2]></image></view>																								
			</view>	
			
			<view class="text-mode">
				<view class="title-mode">我的理想型...</view>
				<view class="normal-line-list">
					<view class="normal-line">· 可我陪我一起在金门跳桥跳海</view>
				</view>				
			</view>
			
			<view class="text-mode">
				<view class="title-mode">我在哪里...</view>
				<view class="normal-line-list">
					<view class="normal-line">北京市 海淀区</view>
				</view>				
			</view>
			
		</view>
	</view>
</template>
 
<script>
	export default {
		data() {
			return {
				current: '0',
				personInfo: {
						// src: "https://up.enterdesk.com/edpic/2e/78/97/2e7897af2087369fbbdf5d0337647489.jpg",
						// name: '提',
						// grade: '/static/mine/head/grade.png',
						// tip: '提港风个性签名...',
						// mag: '你们谎话连篇还以为没人会知道，但有两个人会知道。你们的上帝。还有赫尔克里·波洛。',
						icon: [{
								src: '/static/mine/like/forward.png',
								num: '2234235'
							},
							{
								src: '/static/mine/like/comment.png',
								num: '906478'
							},
							{
								src: '/static/mine/like/like.png',
								num: '45655'
							},
						],
						pic: [
							"https://data.whicdn.com/images/314418661/original.png",
							"https://assets.teenvogue.com/photos/5582ef4dda6f764c6e5611dd/16:9/w_2560%2Cc_limit/celebrity-style-look-of-the-day-2012-11-krysten-ritter-big.jpg",
							"https://taylornetworkofpodcasts.com/wp-content/uploads/2015/09/krysten-ritter-photoshoot-for-dog-saving-campaign-does-whatever-it-takes-_1.jpg",							
							"https://pic2.zhimg.com/80/v2-f088bab4e6da49e600ef3ac225e842a5_720w.jpg?source=1940ef5c",
							"https://pic2.zhimg.com/80/v2-f088bab4e6da49e600ef3ac225e842a5_720w.jpg?source=1940ef5c",
							"https://img9.doubanio.com/view/photo/l/public/p2156921263.webp"
						]
					}
			}
		},
		methods: {
			change(index) {
				this.current = index;
			}
		}
	}
</script>
 
<style scoped lang="scss">
	.sticky {
		width: 750rpx;
		height: 120rpx;
		background-color: #2979ff;
		color: #fff;
		padding: 24rpx;
	}
 
	.like-photo {
		width: 650rpx;
		display: flex;
		flex-wrap: wrap;
		align-items: center;
		justify-content: center;
		margin: 25rpx auto;
		text-decoration: none;
		.cover-image-item {			
			width: 650rpx;
			height: 950rpx;
			margin-bottom: 20rpx;
			position: relative;
			image {
				width: 650rpx;
				height: 950rpx;
				border-radius: 40rpx;
			}
			.user-name {
				width: 500rpx;
				height: 200rpx;
			    top: 770rpx;
				left: 10px;
				margin-bottom: 20rpx;
				position: absolute;
				color: #FFFFFF;
				font-size:150%;
				text-shadow: 1px 1px 0 #000000;
			}
			.user-job {
				width: 500rpx;
				height: 180rpx;
			    top: 850rpx;
				left: 10px;
				margin-bottom: 20rpx;
				position: absolute;
				color: #FFFFFF;
				font-size:100%;
				text-shadow: 1px 1px 0 #000000;
			}
			.user-school {
				width: 500rpx;
				height: 180rpx;
			    top: 900rpx;
				left: 10px;
				margin-bottom: 20rpx;
				position: absolute;
				color: #FFFFFF;
				font-size:100%;
				text-shadow: 1px 1px 0 #000000;
			}
		};
		.normal-image-item {
			width: 650rpx;
			height: 365rpx;
			margin-bottom: 20rpx;
			image {
				width: 650rpx;
				height: 365rpx;
				border-radius: 40rpx;
			}
		}
	}
	
	.text-mode {
		width: 650rpx;
		display: flex;
		flex-wrap: wrap;
		display: block; // 每个块级元素都从新的一行开始，并且其后的元素也另起一行
		margin: 25rpx auto;
		margin-bottom: 50rpx;
		margin-top: 50rpx;
	}
	
	//整体板块
	.user-like-info {
		background: #EBF4FF;
		
		/*弹性布局*/
		align-items: center;
		justify: end;
	}
	
	.basic-info {
	  display: flex;
	  flex-direction:row;
	  flex-wrap:wrap;
	}
 
	// 身高家乡等基本信息
	.basic-info-mode {	
		margin-top:15rpx;
		margin-bottom:15rpx;
		margin-right: 45rpx;
		border-radius: 15rpx;
		border-style:solid;
		border-width:0.5px;
		border-color:#B0E0E6;
		background: #FFFFFF;
		padding:15rpx 20rpx;
		font-size:80%;
		white-space:nowrap;
	}
	
	// 普通兴趣行列表
	.normal-line-list {
		
			
	}
	
	// 普通兴趣行
	.normal-line {
		margin-top:20rpx;
		margin-bottom:20rpx;
		
	}	
	
	.title-mode {
		margin-top:15rpx;
		margin-bottom:15rpx;
		margin-right: 45rpx;	
		color:#9999FF;				
		padding:15rpx 20rpx;
		font-size:80%;		
	}
	
</style>