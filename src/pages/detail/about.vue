<template>
	<section>
		<header>
			<img src="../../assets/img/about/banner.jpg" class="responsive-img p-show">
			<img src="../../assets/img/about/m_banner.png" class="responsive-img m-show">
		</header>
		<main class="main">
			<div class="intro m-show">
				<img src="../../assets/img/about/m_banner1.png" class="responsive-img">
				<img src="../../assets/img/about/m_banner2.png" class="responsive-img">
				<img src="../../assets/img/about/m_banner3.png" class="responsive-img">
				<img src="../../assets/img/about/m_banner4.png" class="responsive-img">
				<img src="../../assets/img/about/m_banner5.png" class="responsive-img">
			</div>
			<div class="container p-show">
				<div class="flex">
					<div class="flex-item">
						<img src="../../assets/img/about/intro1.png">
						<div class="intro_detail photo">
							<h3>旅拍服务</h3>
							<p>覆盖全球50+目的地 国内10+  境外30+</p>
							<p>客样照+视频 全方位立体化展示</p>
							<p>保证品牌 以加盟商品牌对客服务</p>
							<p>你即刻成为最全面的婚嫁电商平台</p>
							<router-link to="photography" class="link-button"></router-link> 
						</div>
					</div>
					<div class="flex-item">
						<img src="../../assets/img/about/intro2.png">
					</div>
					<div class="flex-item">
						<img src="../../assets/img/about/intro3.png">
						<div class="intro_detail tourism">
							<h3>旅游服务</h3>
							<p>与其他品牌差异化竞争</p>
							<p>获取更高营业额及利润</p>
							<p>客人省时省力快速成交</p>
							<p>你即刻成为像携程一样的旅游电商平台</p>
							<router-link to="tourism" class="link-button"></router-link>
						</div>
					</div>
				</div>
				<div class="flex">
					<div class="flex-item">
						<img src="../../assets/img/about/intro4.png">
					</div>
					<div class="flex-item">
						<img src="../../assets/img/about/intro5.png">
						<div class="intro_detail finance">
							<h3>金融服务</h3>
							<p>为婚嫁·旅游产业进行资本对接</p>
							<p>消费金融、供应链金融服务</p>
							<p>利息低、放款快、产品多</p>
							<p>线上店内全支付通道 超低手续费</p>
							<p>你即刻成为全方位服务的金融公司</p>
							<router-link to="finance" class="link-button"></router-link>
						</div>
					</div>
					<div class="flex-item">
						<img src="../../assets/img/about/intro6.png">
					</div>
				</div>
				<div class="flex">
					<div class="flex-item">
						<img src="../../assets/img/about/intro7.png">
						<div class="intro_detail system">
							<h3>系统服务</h3>
							<p>婚嫁／旅游产业转型电商</p>
							<p>PC端、移动端、微信、APP定制开发</p>
							<p>行业属性多渠道分销系统</p>
							<p>让每个人都可以成为你的销售</p>
							<p>你即刻成为全系统的科技公司</p>
							<router-link to="system" class="link-button"></router-link>
						</div>
					</div>
					<div class="flex-item">
						<img src="../../assets/img/about/intro8.png">
					</div>
					<div class="flex-item">
						<img src="../../assets/img/about/intro9.png">
						<div class="intro_detail marketing">
							<h3>网络营销</h3>
							<p>网络多渠道流量整合</p>
							<p>百度、腾讯、微博、今日头条、大众点评…</p>
							<p>SEO、SEM</p>
							<p>品牌推广、产品推广、事件营销…</p>
							<p>你即刻成为全方位网络互动营销公司</p>
							<router-link to="marketing" class="link-button"></router-link>
						</div>
					</div>
				</div>
			</div>
			<div class="m-show">
				<img src="../../assets/img/about/m_banner6.png" class="responsive-img">
				<img src="../../assets/img/about/m_banner7.png" class="responsive-img">
				<img src="../../assets/img/about/m_banner8.png" class="responsive-img">
			</div>
			<!-- <div class="yue-about p-show">
				<div class="container">
					<img src="../../assets/img/about/about_view.jpg" alt="">
					<img src="../../assets/img/about/about_text_bg.png" alt="">
				</div>
			</div> -->
			<div class="p-show">
				<img src="../../assets/img/about/view.jpg" class="responsive-img">
				<div class="about-wrap">
					<img src="../../assets/img/about/about_bg.jpg" class="responsive-img">
					<div class="about-content container">
						<div class="about-left">
							<div class="logo"></div>
							<div class="date">{{currentDate}}</div>
						</div>
						<div class="about-right">
							<div class="about-detail">
								<div class="detail-left">
									<div class="title"><strong>选择悦视觉</strong> <i>您将得到什么？</i></div>
									<span class="underline"></span>
									<p>让所有与我们合作的企业 轻松的赚到钱</p>
									<p>与我们在一起 会发现 得到的不只是以上</p>
									<span class="line"></span>
									<strong class="more">还有更多</strong>
									<p>真正让你们企业成为</p>
									<p>跨行业 跨区域 跨国家</p>
									<p>真正全球化的企业</p>
									<span class="line bottom"></span>
								</div>
								<div class="detail-right">
									<ul class="icon-list">
										<li><span></span></li>
										<li><span></span></li>
										<li><span></span></li>
										<li><span></span></li>
									</ul>
								</div>
							</div>
						</div>
					</div>
				</div>
				<img src="../../assets/img/about/process.png" class="responsive-img">
			</div>
		</main>
	</section>
</template>
<script>
	export default {
		computed: {
			currentDate() {
				let date = new Date();
				let month = date.getMonth() + 1,
						day = date.getDate(),
						hour = date.getHours(),
						minutes = date.getMinutes();
				let text = hour < 12 ? 'am' : 'pm';
				month = month < 10 ? '0' + month : month;
				day = day < 10 ? '0' + day : day;
				minutes = minutes < 10 ? '0' + minutes : minutes;
				return date.getFullYear() + '.' + month + '.' + day + ' ' + hour + ':' + minutes+text;
			}
		},
		mounted () {
			window.scrollTo(0, 0);
		}
	}
</script>
<style scoped lang="scss">
	.main {
		width: 100%;
		margin: 0 auto;
		.intro {
			padding: 15px;
		}
		.container {
			max-width: 1180px;
			width: 80%;
			margin: 30px auto;
		}
		// @media(min-width: 1200px) {
		// 	width: 70%;
		// }
		// @media(min-width: 1440px) {
		// 	width: 80%;
		// }
		// @media(min-width: 1900px) {
		// 	width: 60%;
		// }
	}
	.flex-item {
		position: relative;
		img {
			width: 100%;
			height: 100%;
		}
	}
	.intro_detail {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		padding: 1.5rem;
		color: #fff;
		&.photo {
			background: #62B5E4;
			h3 {
				margin: 20px 0;
			}
		}
		&.tourism {
			background: #656E81;
			h3 {
				margin: 20px 0;
			}
		}
		&.finance {
			color: #666;
			background: #FEFAFA;
			.link-button {
				background: url(../../assets/img/about/button_arrow_gray.png) no-repeat center;
				background-size: cover;
			}
			&:hover {
				.link-button {
					background: url(../../assets/img/about/button_more_gray.png) no-repeat center;
					background-size: cover;
				}
			}
		}
		&.system {
			background: #656E81;
		}
		&.marketing {
			background: #2CB0BA;
		}
		h3 {
			margin: 5px 0;
			font-size: 24px;
			letter-spacing: 1px;
			@media (min-width: 1200px) {
				margin: 10px 0;
				font-size: 28px;
			}
		}
		p {
			font-size: 14px;
			line-height: 1.5;
			word-break: keep-all;
			white-space: nowrap;
			overflow: hidden;
			text-overflow: ellipsis;
			@media (min-width: 1200px) {
		    font-size: 16px;
		    line-height: 1.8;
		  }
		  @media (min-width: 1900px) {
		    font-size: 16px;
		    line-height: 2.2;
		  }
		}
		.link-button {
			position: absolute;
			left: 10px;
			bottom: 10px;
			display: block;
			width: 10px;
			height: 10px;
			margin-top: .3rem;
			background: url(../../assets/img/about/button_arrow.png) no-repeat center;
			background-size: cover;
			transition: all .2s;
			@media (min-width: 768px) {
				left: 30px;
				width: 32px;
				height: 32px;
				bottom: 15px;
			}
			@media (min-width: 1200px) {
				width: 32px;
				height: 32px;
				bottom: 20px;
			}
		}
		&:hover {
			.link-button {
				width: 104px;
				height: 32px;
				background: url(../../assets/img/about/button_more.png) no-repeat center;
				background-size: cover;
			}
		}
	}
	.about-wrap {
		position: relative;
		.about-content {
			position: absolute;
			top: 10%;
			left: 0;
			right: 0;
			width: 80%;
			height: 80%;
			margin: auto;
			@media(min-width: 1200px) {
				top: 15%;
				height: 70%;
			}
			// @media(min-width: 1900px) {
			// 	top: 20%;
			// 	height: 60%;
			// }
			.about-left {
				position: absolute;
				top: 0;
				left: 0;
				bottom: 0;
				width: 45%;
				padding: 2rem;
				background: url(../../assets/img/about/about_view.jpg);
				background-size: 100% 100%;
				.logo {
					width: 38%;
					height: 32%;
					max-width: 192px;
					max-height: 116px;
					background: url(../../assets/img/about/about_logo.png) no-repeat center;
					background-size: 100% 100%;
				}
				.date {
					position: absolute;
					margin: -1.2rem 2.5rem;
					font-size: 1rem;
					color: #fff;
				}
			}
			.about-right {
				position: absolute;
				top: 2rem;
				bottom: 2rem;
				right: 0;
				width: 62%;
				padding: 1rem 2rem;
				background: url(../../assets/img/about/about_text_bg.png);
				background-size: cover;
				box-shadow: 1px 1px 1px 1px #ccc;
				// @media (min-width: 1440px) {
				// 	padding: 2.5rem
				// }
				@media (min-width: 1900px) {
					padding: 3rem 4rem
				}
				.about-detail {
					display: flex;
					.detail-left {
						flex: 1;
						@media(min-width: 1900px) {
							padding-top: 15px;
						}
						.title {
							font-size: 20px;
							@media(min-width: 1200px) {
								margin: 10px 0;
								font-size: 22px;
							}
							@media(min-width: 1440px) {
								margin: 15px 0;
							}
							@media(min-width: 1900px) {
								font-size: 26px;
							}
							i {
								font-style: normal;
								color: #666;
							}
						}
						p {
							line-height: 1.6;
							font-size: 12px;
							color: #666;
							@media (min-width: 1200px) {
								font-size: 14px;
							}
							@media (min-width: 1900px) {
								font-size: 16px;
								line-height: 2;
							}
						}
						.more {
							line-height: 2;
							font-size: 14px;
							@media (min-width: 1200px) {
								font-size: 16px;
							}
						}
						.underline {
							display: block;
							width: 2rem;
							height: 2px;
							margin: 5px 0;
							background: #333;
							@media (min-width: 1200px) {
								margin: 10px 0;
							}
						}
						.line {
							display: block;
							width: 80%;
							height: 1px;
							margin: 10px 0;
							background: #888;
							&.bottom {
								width: 90%;
								margin-top: 0.6rem;
							}
						}
					}
					.detail-right {
						width: 4rem;
						.icon-list {
							display: flex;
							flex-direction: column;
							height: 100%;
							@media (min-width: 1440px) {
								margin-top: 15px;
							}
							li {
								flex: 1;
								padding-top: 10px;
								text-align: center;
								span {
									display: inline-block;
									width: 25px;
									height: 25px;
									transition: all .2s;
								}
								&:first-child {
									span {
										background: url(../../assets/img/about/icon1.png) no-repeat center;
										background-size: cover;
									}
									&:hover {
										span {
											width: 40px;
											height: 40px;
											background: url(../../assets/img/about/icon1_active.png) no-repeat center;
											background-size: cover;
										}
									}
								}
								&:nth-child(2) {
									span {
										background: url(../../assets/img/about/icon2_active.png) no-repeat center;
										background-size: cover;
									}
									&:hover {
										span {
											width: 40px;
											height: 40px;
											background: url(../../assets/img/about/icon2_active.png) no-repeat center;
											background-size: cover;
										}
									}
								}
								&:nth-child(3) {
									span {
										background: url(../../assets/img/about/icon3.png) no-repeat center;
										background-size: cover;
									}
									&:hover {
										span {
											width: 40px;
											height: 40px;
											background: url(../../assets/img/about/icon3_active.png) no-repeat center;
											background-size: cover;
										}
									}
								}
								&:nth-child(4) {
									span {
										background: url(../../assets/img/about/icon4.png) no-repeat center;
										background-size: cover;
									}
									&:hover {
										span {
											width: 40px;
											height: 40px;
											background: url(../../assets/img/about/icon4_active.png) no-repeat center;
											background-size: cover;
										}
									}
								}
							}
						}
					}
				}
			}
		}
	}
</style>