<template>
  <div class="login">
      <div class="login_wrapper">
      <div class="animate form login_form">
        <section class="login_content">
          <form>
            <h1>管理员登录</h1>
            <div>
              <input type="text" class="form-control" v-model="userName" placeholder="管理员登录名" required />
            </div>
            <div>
              <input type="password" class="form-control" v-model="userPwd" placeholder="管理员登录密码" required />
            </div>
            <div>
              <a class="btn btn-default submit" @click="loginToIndex">&nbsp;登&nbsp;录&nbsp;</a>
            </div>

            <div class="clearfix"></div>

            <div class="separator">
              <div class="clearfix"></div>
              <br />

              <div>
                <h1><i><img src="../assets/img/favicon.ico"></i> 学子商城后台管理系统</h1>
                <p>©2017 版权所有，CODEBOY.COM</p>
              </div>
            </div>
          </form>
        </section>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data:function(){
      return {
          msg:'Hello Login',
          userName:'',
          userPwd:''
      }
  },
  mounted:function(){
      console.log('挂载完毕');
      
  },
  methods:{
      loginToIndex:function(){
            console.log(this.userName,this.userPwd);
            this.$http.get('http://Jsonplaceholder.typicode.com/posts?userName='+this.userName).then(function(response){
                 console.log(response.data);
                 this.$router.push('index');
            });
      }
  }
}
</script>
<style>

</style>


