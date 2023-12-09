<template>
  <div class="login-feild">
    <form class="login-form">
      <p><input type="text" v-model="email" placeholder="メールアドレス" name="email" class="user-email" /></p>
      <p><input type="text" v-model="password" placeholder="パスワード" name="password" class="user-password" /></p>
      <div>
        <button type="submit" class="login-form-btn">ログイン</button>
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data () {
    return {
      email: '',
      password: ''
    }
  }
}
</script>

<style scoped>
.login-field {
  margin: 50%;
}
.user-email {
    width: 50%;
    height: 8vh;
    margin: auto;
    text-align: center;
    color: black;
}
.user-password {
  width: 50%;
  height: 8vh;
  margin: auto;
  text-align: center;
  color: black;
}

.login-form {
  text-align: center;
  margin-top: 30vh;
}
.login-form-btn {
  width: 30%;
  height: 6vh;
  text-align: center;
}

</style>
