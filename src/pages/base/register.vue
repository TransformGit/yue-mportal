<template>
	<section>
		<div class="login-bg">
			<div class="login-box">
				<div class="login-top">
					<img src="../../assets/img/login/logo.png" alt="">
				</div>
				<div class="login-content">
					<div class="register-link">
						<span>已经注册？<router-link to="login">马上登录>></router-link></span>
					</div>
					<form class="login-form" onsubmit="return false">
						<div class="form-item">
							<label class="form-item__label" for="partnerName">企业名称</label>
							<input type="text" id="partnerName" v-model="form.partnerName" class="form-item__input" required>
						</div>
						<!-- <div class="form-item">
							<label class="form-item__label">企业网址(选填)</label>
							<input type="text" v-model="form.partnerSite" class="form-item__input">
						</div> -->
						<div class="form-item">
							<label class="form-item__label" for="contactName">联系人</label>
							<input type="text" id="contactName" v-model="form.contactName" class="form-item__input" required>
						</div>
						<div class="form-item">
							<label class="form-item__label" for="titleName">职务</label>
							<input type="text" id="titleName" v-model="form.titleName" class="form-item__input" required>
						</div>
						<div class="form-item">
							<label class="form-item__label" for="email">邮箱</label>
							<input type="email" id="email" v-model="form.email" class="form-item__input" required>
						</div>
						<div class="form-item">
							<label class="form-item__label" for="password">密码</label>
							<input type="password" id="password" v-model="form.password" class="form-item__input" maxlength="16" required>
						</div>
						<div class="form-item">
							<label class="form-item__label" for="password2">确认密码</label>
							<input type="password" id="password2" v-model="form.password2" class="form-item__input" maxlength="16" required>
						</div>
						<div class="form-item">
							<label class="form-item__label" for="mobile">手机号</label>
							<input type="mobile" id="mobile" v-model="form.mobile" class="form-item__input"  maxlength="11" required>
						</div>
						<div class="form-item">
							<label class="form-item__label" for="smsCode">手机验证码</label>
							<input type="text" id="smsCode" v-model="form.smsCode" class="form-item__input" maxlength="6" required>
							<button type="button" class="form-item__button" :disabled="disabled" @click="getSmsCode">{{buttonText}}</button>
						</div>
						<div class="form-item submit">
							<mt-button native-type="submit" type="primary" @click="submitForm">立即注册</mt-button>
						</div>
					</form>
				</div>
			</div>
		</div>
	</section>
</template>
<script>
	import Md5 from '@/assets/js/md5'
	import { requestRegist, getMobileSmsCode } from '@/api'
	export default {
		data () {
			return {
				form: {
					partnerName: '',
					contactName: '',
					titleName: '',
					mobile: '',
					smsCode: '',
					email: '',
					password: '',
					password2: ''
				},
				disabled: false,
				buttonText: '获取验证码',
			}
		},
		methods: {
			countDown() {
				let count = 60;
				let timer = null;
				this.disabled = true;
				timer = setInterval(() => {
					if(count > 0) {
						this.buttonText = `重新获取 ${count}s`
						count --;
					} else {
						this.buttonText = '重新获取';
						this.disabled = false;
						clearInterval(timer)
					}
				}, 1000)	
			},
			getSmsCode(e) {
				if(!this.form.mobile.match(/^(13|14|15|17|18)\d{9}$/)){
					this.$toast({
						title: '提示',
						message: '请填写正确手机号码',
					})
					return;
				}
				let params ={
					mobile: this.form.mobile
				}
				// this.countDown();
				getMobileSmsCode(params).then(res => {
					console.log(res)
					if(res.data.code === '0001') {
						this.countDown();
					} else {
						this.$toast(res.data.message)
					}
				}).catch(err => {
					console.log(err)
					this.$catchError(err)
				})
			},
			submitForm() {
				let data = Object.assign({}, this.form)
				for(let i in data) {
					if(!data[i]) return;
				}
				if(this.form.password !== this.form.password2) {
					this.$toast({
						title: '提示',
						message: '两次密码输入不一致',
					})
					return;
				}
				if(!this.form.mobile.match(/^(13|14|15|17|18)\d{9}$/)) {
					this.$toast({
						title: '提示',
						message: '请输入正确手机号码',
					})
					return;
				}
				data.password = Md5.hex_md5(this.form.password)
				data.password2 = Md5.hex_md5(this.form.password2)
				requestRegist(data).then(res => {
					if(res.data.code === '0001') {
						this.$router.push('/register_success')
					} else {
						this.$toast(res.data.message)
					}
				}).catch(err => {
					console.log(err)
					this.$catchError(err)
				})
			},
		}
	}
</script>
<style scoped lang="scss">
	.login-bg {
		display: flex;
		justify-content: center;
		align-items: center;
		height: auto;
		padding: 30px;
		background: url(../../assets/img/login/register_bg.jpg) no-repeat center;
		background-size: cover;
		.login-box {
			width: 100%;
			text-align: center;
			@media (min-width: 768px) {
			  width: 400px;
			}
			.login-top {
				width: 60%;
				margin: auto;
				@media (min-width: 768px) {
				  width: 80%;
				}
			}
			.login-content {
				margin: 15px 0;
				padding: 15px 30px 20px;
				background: rgba(255,255,255,.8);
				@media (min-width: 768px) {
				  margin: 30px 0;
				}
				.register-link {
					font-size: 14px;
					text-align: right;
					a {
						color: #009ae0;
					}
				}
				.mint-button {
					width: 100%;
					// margin-top: 10px;
					border-radius: 0;
					color: #fff;
					font-size: 18px;
				}
			}
		}
	}
</style>