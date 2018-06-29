<template>
<div class="login  hide">
  <div class="login-container">
    <div class="login-pop-title">登录
      <div class="login-close close" @click="closed">
      </div>
    </div>
    <div class="login-pop-content">
      <form role="form" id="signInForm" novalidate="novalidate">
        <div class="form-group">
          <label for="username">用户名</label>
          <input type="text" class="form-control" id="username" name="username" placeholder="请输入用户名">
        </div>
        <div class="form-group">
          <label for="password">密码</label>
          <input type="password" class="form-control" id="password" name="password" placeholder="请输入密码">
        </div>
        <p class="sure">
            <label>
		        <input class="form-check-input" name="over18" type="checkbox" checked="checked" style="margin-right: 8px;">我确认我已年满18周岁，并已阅读和确认本网站的策略，隐私声明、<a>条款及条件</a>
		    </label>
        </p>
        <p class="warn"></p>
        <p class="butn"><button type="button" class="btn signInBtn" id="btnLogin">登&nbsp;&nbsp;录</button></p>
      </form>
    </div>
  </div>
</div>
</template>

<script>
	import Hub from '@/components/Hub';	
export default {
  data(){
  	return {


  	}
  },
  methods: {
      closed(){
    	Hub.$emit('closed',false);
    },
  },
}
</script>

<style lang="scss" scoped>
	.login{
		width: 100%;
    height: 100%;
    position: fixed;
    top: 0;
    z-index: 2000001;
    left: 0;
    background-color: rgba(0,0,0,.6);
		.login-container{
			 width: 460px;
        margin: 10% auto;
			.login-pop-title {
            position: relative;
            height: 38px;
            background-color: #f07;
            color: #fff;
            line-height: 38px;
            font-size: 16px;
            padding-left: 10px;
            .login-close {
                background-image: url("../../static/v2-login-pop-close.png");
                width: 18px;
                height: 18px;
                position: absolute;
                top: 10px;
                right: 10px;
                cursor: pointer;
            }
        }
			.login-pop-content{
				background-color: #fff;
        padding: 20px 25px;
				form{
					.form-group {
                margin-left: -15px;
                margin-right: -15px;
                label {
                    font-size: 16px;
                    color: #333;
                    font-weight: 400;
                    padding: 7px 0 0;
                    width: 70px;
                }
                .form-control {
                    height: 42px;
                    line-height: 42px;
                    font-size: 16px;
                    color: #666!important;
                    border: 1px solid #ddd;
                    border-radius: 2px;
                    width: 270px;
                    padding: 0 12px;
                    margin-bottom: 15px;
                }
                .input-group-addon {
                    img {}
                }

            }
					.sure {
                label {
                    display: inline-block;
                    max-width: 100%;
                    margin-bottom: 5px;
                    .form-check-input {
                        margin-right: 8px;

                        font-size: 12px;
                        color: #333;
                        -webkit-font-smoothing: antialiased;
                    }
                }
            }
					.warn {
                color: #f07;
                padding: 7px;
            }
            .butn {
                width: 410px;
                text-align: center;
                button {
                    height: 38px;
                    width: 270px;
                    line-height: 38px;
                    background-color: #f07;
                    font-size: 16px;
                    border-radius: 2px;
                    color: #fff;
                }
            }
				}
			}
		}
	}
</style>
