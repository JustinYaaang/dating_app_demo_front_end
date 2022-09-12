<template>
	<view>
		<!-- 页面顶部导航栏 -->
		<view>
			<u-navbar title="我的赞" title-color="#25AFA2" 
            back-icon-name="nav-back" back-icon-color="#25AFA2"
				back-text="返回"></u-navbar>
		</view>
		<!-- 切换赞&收藏版块 -->
		<view>
			<u-sticky>
				<!-- 只能有一个根元素 -->
				<u-tabs name="cate_name" :list="list" :is-scroll="false" 
               :current="current" @change="change"
					inactive-color="#999999" active-color="#25AFA2"></u-tabs>
			</u-sticky>
		</view>
		<view class="user-like-info" v-for="(item,index) in articleList">
			<view class="uer-line"></view>
			<!-- 用户头像、昵称、版块 -->
			<view class="like-artive">
				<u-avatar :src="item.src" mode="circle" :show-level="true" level-bg- 
                  color="#25AFA2" class="head-img">
				</u-avatar>
				<view class="like-meg">
					<view class="like-meg-info">
						<view class="like-meg-title">{{item.name}}</view>
						<image class="like-meg-item" :src="item.grade"></image>
					</view>
					<view class="like-meg-tip">{{item.tip}}</view>
				</view>
				<view class="like-botton">+收藏</view>
			</view>
			<!-- 文章发布内容 -->
			<view class="like-content">{{item.mag}}​​​​</view>
			<view class="like-photo">
				<!-- 发布文章时的图片 -->
				<view class="like-photo-item" v-for="(imagesSrc,i) in item.pic">
					<image :src="imagesSrc"></image>
				</view>
			</view>
			<!-- 评论点赞板块 -->
			<view class="like-data">
				<view class="like-data-item" v-for="(itemicon,i) in item.icon">
					<image class="like-data-icon" :src="itemicon.src"></image>
					<view class="like-data-num">{{itemicon.num}}</view>
				</view>
			</view>
		</view>
	</view>
</template>
 
<script>
	export default {
		data() {
			return {
				list: [{
						cate_name: '赞'
					},
					{
						cate_name: '收藏'
					},
				],
				current: '0',
				articleList: [{
						src: "https://up.enterdesk.com/edpic/2e/78/97/2e7897af2087369fbbdf5d0337647489.jpg",
						name: '提',
						grade: '/static/mine/head/grade.png',
						tip: '提港风个性签名...',
						mag: '你们谎话连篇还以为没人会知道，但有两个人会知道。你们的上帝。还有赫尔克里·波洛。',
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
							    "https://pic2.zhimg.com/80/v2-f088bab4e6da49e600ef3ac225e842a5_720w.jpg?source=1940ef5c",
							"https://pic2.zhimg.com/80/v2-f088bab4e6da49e600ef3ac225e842a5_720w.jpg?source=1940ef5c",
							"https://pic2.zhimg.com/80/v2-f088bab4e6da49e600ef3ac225e842a5_720w.jpg?source=1940ef5c",
							"https://pic2.zhimg.com/80/v2-f088bab4e6da49e600ef3ac225e842a5_720w.jpg?source=1940ef5c",
							"https://pic2.zhimg.com/80/v2-f088bab4e6da49e600ef3ac225e842a5_720w.jpg?source=1940ef5c",
							"https://pic2.zhimg.com/80/v2-f088bab4e6da49e600ef3ac225e842a5_720w.jpg?source=1940ef5c"
						]
					},
					{
						src: 'https://up.enterdesk.com/edpic/2e/78/97/2e7897af2087369fbbdf5d0337647489.jpg',
						name: ' 加藤オズワルト',
						grade: '/static/mine/head/grade.png',
						tip: ' 加藤オズワルト个性签名...',
						mag: '来自插画师 加藤オズワルド  绘画作品来自插画师 加藤オズワルド绘画作品来自插画师 加藤オズワルド  绘画作品',
						icon: [{
								src: '/static/mine/like/forward.png',
								num: '22'
							},
							{
								src: '/static/mine/like/comment.png',
								num: '553578'
							},
							{
								src: '/static/mine/like/like.png',
								num: '987655'
							},
						],
						pic: [
							"https://pic3.zhimg.com/80/v2-fa4664732e8ec7b3da68bfa414477fa6_720w.jpg?source=1940ef5c",
							"https://pic3.zhimg.com/80/v2-fa4664732e8ec7b3da68bfa414477fa6_720w.jpg?source=1940ef5c",
							"https://pic3.zhimg.com/80/v2-fa4664732e8ec7b3da68bfa414477fa6_720w.jpg?source=1940ef5c"
						]
					}
				]
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
 
	.uer-line {
		margin-top: 15rpx;
		width: 750rpx;
		height: 14rpx;
		opacity: 1;
		background: #f1f1f1;
	}
 
	.like-artive {
		display: flex;
		width: 700rpx;
		height: 80rpx;
		margin: 20rpx auto;
		.like-meg {
			padding-left: 20rpx;
 
			.like-meg-info {
				display: flex;
				padding-bottom: 15rpx;
 
				.like-meg-title {
					font-size: 30rpx;
					font-family: Microsoft YaHei, Microsoft YaHei-Regular;
					font-weight: bold;
					text-align: left;
					color: #333333;
				}
				.like-meg-item {
					width: 30rpx;
					height: 30rpx;
					padding-left: 12rpx;
				}
			}
 
			.like-meg-tip {
				font-size: 20rpx;
				font-family: Microsoft YaHei, Microsoft YaHei-Regular;
				font-weight: 400;
				text-align: left;
				color: #63a4e9;
			}
		}
 
		.like-botton {
			width: 120rpx;
			height: 60rpx;
			background: #25afa2;
			border-radius: 30px;
			font-size: 24rpx;
			line-height: 60rpx;
			font-family: Microsoft YaHei, Microsoft YaHei-Regular;
			font-weight: 400;
			text-align: center;
			color: #ffffff;
			margin-left: auto;
		}
	}
 
	.like-content {
		width: 700rpx;
		margin: 25rpx auto 30rpx;
		font-size: 28rpx;
		font-family: Microsoft YaHei, Microsoft YaHei-Regular;
		font-weight: 400;
		text-align: left;
		color: #333333;
		line-height: 42rpx;
	}
 
	.like-photo {
		width: 700rpx;
		display: flex;
		flex-wrap: wrap;
		justify-content: space-between;
		margin: 25rpx auto;
		text-decoration: none;
		.like-photo-item {
			width: 220rpx;
			height: 220rpx;
			margin-bottom: 20rpx;
			image {
				width: 220rpx;
				height: 220rpx;
			}
		}
	}
 
	.like-data {
		display: flex;
		/*弹性布局*/
		align-items: center;
		/*子元素垂直居中*/
		justify-content: center;
		/*子元素水平居中*/
		justify-content: space-around;
		/*子元素充满父元素*/
		border-top: 1rpx solid #E1E1E1;
		.like-data-item {
			display: flex;
			margin-top: 30rpx;
			margin-bottom: 10rpx;
 
			.like-data-icon {
				width: 34rpx;
				height: 34rpx;
			}
			.like-data-num {
				padding-left: 15rpx;
				font-size: 24rpx;
				font-family: Microsoft YaHei, Microsoft YaHei-Regular;
				font-weight: 400;
				text-align: left;
				color: #666666;
			}
		}
	}
</style>